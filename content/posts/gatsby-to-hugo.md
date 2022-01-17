---
title: "Gatsby to Hugo"
date: 2020-08-15T12:09:01-05:00
shortname: "g2h"
draft: false
---

Recently, I wanted to update my website for the sake of having something new and different.
When I opened up my the repository for my older website, I was taken back by the sheer complexity that Gatsby requires. 
I thought that updating my website would prove to be a headache.
Gatsby uses GraphQL to get custom data from the file system, in my case a bunch of Markdown files.
Having to rewrite or copy-paste GraphQL queries seemed kind of daunting to me since I'm unfamiliar with GraphQL, as well as making sure that all of my needed files where found by Gatsby.

After some reflection, I realized that Gatsby was too complex for my use case.
It got the job done, but I remember Gatsby being a bit of a headache to get up and running.
However, Gatsby seemed nice in generating static sites where the data could be from any API, but for me it was just Markdown files and plenty of other frameworks did that.

Jekyll, another popular static site generator and GitHub Page's choice, seemed like a viable option. 
I recently used it for my DREU website and were supposed to directly fork an example repository that used a basic Jekyll starter theme.
The setup and adding content was simple enough, but to me it felt like a couple of things were hidden from view such as the layout of the site.
Additionally, the Jekyll theme did not seem to follow Jekyll standards so it was confusing if I needed help with something.

Another option I looked into was Hugo. I remember seeing a friend using it for their personal website so I decided to give it a try.
After looking into documentation and example Hugo websites, one of the things that stuck out to me was Hugo's themes. 
Unlike my DREU Jekyll site, the theme files were not incorporated throughout the project.
Instead, themes go in a separate folder and you can specify which theme you want in the site's `config.toml` file.
Ideally, you can have your site's content incorporated into any Hugo theme without changing too much, however Hugo themes can still be highly customizable.

After taking a look at multiple Hugo themes, none of them had the simplicity that I was looking for. So instead, I made my own theme with features from another theme I liked.
For instance, social icons can take a while to implement yourself so instead I used the social.html partial from the theme. Themes can have `archetypes` which are like types of content such as a blog post.
For my theme, I added a project archetype so that I can have list of projects to show off in my theme. 

After using Hugo for a bit, I found Hugo much faster than Gatsby when building the site on Netlify. And I'm happy with this framework and the flexibility it provides for my simple Markdown blog.


