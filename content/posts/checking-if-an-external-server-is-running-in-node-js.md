---
title: Checking if an external server is running in Node.js
shortname: ext-svr
date: 2022-01-17T19:51:33.945Z
draft: false
---
At Rivet, our testing process involves external services such as our PostgreSQL, ElasticSearcn and sometimes an API to mock third-party services. Each test specifies which services it depends on, we then start those services and run a health check to see if they're running before the test begins.

Some services have a nice way to check if they're running. PostgreSQL has `pg_isready` with a timeout parameter and check for a zero exit code and ElasticSearch has the `/_cluster/health` which we can check for a status code of 200. However, sometimes a service doesn't provide a built-in way to check for the health and/or status of a service. An alternative way is to see if the server itself is ready to accept connections with a socket:

```typescript
const checkService = async (host: number, port: string, timeout: number) => {
  const promise = new Promise<string | null>((res, rej) => {
    const socket = new net.Socket();

    const onError = (msg: string) => () => {
      socket.destroy();
      rej(msg);
    };

    socket.setTimeout(1000);
    socket.once('error', err => onError(String(err))());
    socket.once('timeout', onError('Connection timeout'));

    socket.connect(port, host, () => {
      socket.end();
      res(null);
    });
  });

  try {
    return await promise;
  } catch (e: any) {
    return e;
  }
}
```

A somewhat annoying aspect of JavaScript are event listeners. They offer a little convenience, where you can setup a socket and then add listeners to handle different tasks. In this case, they didn't allow us to "await" until a connection was established, we had to set up a callback. Additionally, we can't directly return from a callback. For instance, in the `socket.connect` callback, we can return a value, but it won't be picked up by the outer function since it will be out of scope. We could add a variable outside of the callback and update it in the callback, but that introduces side effects. The nice thing with Promises is that they provide callback functions in an "on success" and "on error" situation. These will either return a value or throw an error.

