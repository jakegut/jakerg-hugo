---
title: Self Taught Operating Systems
date: 2022-01-12T02:05:09.972Z
shortname: 'st-os'
draft: false
---
## tl;dr

I'm learning operating systems thanks to [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/), check out my ["syllabus"](#syllabus).

## Intro

I've been interested in learning more about Operating Systems for quite some time now, so much so I've considered going to grad school to learn more about it. However, I think I can make do with the resources available online. I just won't have anything to show for it besides personal projects, as opposed to a post-undergraduate education.

## Information Overload

With so much information online, it's overwhelming shifting through it all and deciding which resource is the "best". When trying to learn more about anything Computer Science related, I like to see if there's a book on the subject. So, I looked up some threads about books to learn more about Operating Systems and I came across a few books:

* ["OSTEP"](https://pages.cs.wisc.edu/~remzi/OSTEP/) -- Operating Systems: Three Easy Pieces by Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau
* [The "dinosaur" book](https://codex.cs.yale.edu/avi/os-book/OS10/index.html) -- Operating System Concepts by Silberschatz, et al.
* [Modern Operating Systems](https://www.pearson.com/us/higher-education/program/Tanenbaum-Modern-Operating-Systems-4th-Edition/PGM80736.html) by Tanenbaum

OSTEP was the most mentioned book and is even featured on [Teach Yourself CS](https://teachyourselfcs.com/#operating-systems). OSTEP has individual chapters for free online and has [multiple projects](https://github.com/remzi-arpacidusseau/ostep-projects) to do. The dinosaur book has projects as well, but what I like most about OSTEP's set of projects is that about half of them involve extending the xv6 kernel.

I'm glad that I found a book to read and reference to, now I have to find out which parts are relevant. While I eventually want to go through all of it, I'd like some direction on which parts I need to read the most to kickstart my learning. Luckily I found Remzi's course website where he uses OSTEP as the textbook: [UWM CS-537: Intro to Operating Systems](https://pages.cs.wisc.edu/~remzi/Classes/537/Spring2018/). This course includes a lot of useful information such as a calendar, projects, and even videos which is a rare find on course websites.

While the course website is packed with information, I'm often at a loss (dare say, overwhelmed) whenever I visit it. The calendar portion is a bit too packed for me and I often click around and go back and forth between the videos, projects and reading.

The main reason I'm creating this post is to hopefully organize and extend upon the course in a format that I can follow step-by-step and can easily come back to. I'll create a personal syllabus that first includes the Intro to OS course, some more readings and projects from OSTEP and finally another book to apply my knowledge to. 

## A Syllabus {#syllabus}

No dates here, don't want to stress about meeting a certain deadline. Instead, I plan on completing each row-by-row in order. You could probably pace yourself by doing one row a week.

### Intro to OS

Most chapters in OSTEP have accompanying homeworks which can be found [here](https://github.com/remzi-arpacidusseau/ostep-homework/). Lectures here are optional and can range from 20 - 50 minutes long each. For myself, I'm doing each reading listed below with the project. If I feel like the reading wasn't enough I'll do the homework and try to watch the lectures. The "Discussion" for each project is recommended since it explains the project in detail.

| Reading | Lectures | Project | Discussion |
| --- | ----------- | --- | --- | --- |
| Intro & Processes<br>OSTEP Ch. Pre - 6 | [Part 1](https://www.youtube.com/watch?v=3uMbb9dLtlE)<br>[Part 2](https://www.youtube.com/watch?v=K4qbAiC77Yo)<br>[Part 3](https://www.youtube.com/watch?v=LVxN7ZkGh3w)| [Unix Utilities](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/initial-utilities) | [Discussion](https://www.youtube.com/watch?v=rgcq9x8LtGQ) |
| Scheduling<br>OSTEP Ch. 7 - 9 | [Part 1](https://www.youtube.com/watch?v=oTd72Yp2m8w)<br>[Part 2](https://www.youtube.com/watch?v=Q09UgVfragU)<br>[Part 3](https://www.youtube.com/watch?v=fin5-82L-r8)|
| Memory Management & Paging<br>OSTEP Ch. 13 - 16; 18 | [Part 1](https://youtu.be/cAiwISFta4g)<br>[Part 2](https://youtu.be/I0RIlSN0DzM)<br>[Part 3](https://youtu.be/0WVoWlOT-kY)| [Intro To Kernel Hacking](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/initial-xv6) | [Discussion](https://www.youtube.com/watch?v=vR6z2QGcoo8) |
| Paging: TLB & Paging: Smaller<br>OSTEP Ch. 19 - 20 | [Part 1](https://youtu.be/wAx_h3HkIX0)<br>[Part 2](https://youtu.be/7BOXM2XgGO4)<br>[Part 3](https://youtu.be/LprKOBsALGA)| [Unix Shell](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/processes-shell) | [Discussion](https://youtu.be/76PfvXTwF04) |
| Beyond Physical Memory<br>OSTEP Ch. 21 - 22 | [Part 1](https://youtu.be/wAx_h3HkIX0)<br>[Part 2](https://youtu.be/7BOXM2XgGO4)<br>[Part 3](https://youtu.be/LprKOBsALGA)| 
| Threads & Locks<br>OSTEP Ch. 25 - 26; 28 | [Part 1](https://www.youtube.com/watch?v=ggPkFxOTwHY)<br>[Part 2](https://www.youtube.com/watch?v=4tPXkN5nRQs)| [xv6 Lottery Scheduler](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/scheduling-xv6-lottery) | [Discussion](https://www.youtube.com/watch?v=eYfeOT1QYmg) |
| Locks, CVs & More CVs<br>OSTEP Ch. 29 - 30 | [Part 1](https://www.youtube.com/watch?v=4PghlMdp9cU)<br>[Part 2](https://www.youtube.com/watch?v=hivv8F-LjzY)<br>[Part 3](https://youtu.be/BoLYvNp2Lc4)|
| Semaphores<br>OSTEP Ch. 31 | [Part 1](https://youtu.be/U1LfmL7f1h8)<br>[Part 2](https://youtu.be/cuY8r8RXqAY)<br>[Part 3](https://youtu.be/WVHRaqom0yo)| [Parallel Zip](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/concurrency-pzip)<br>[xv6 Virtual Memory](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/vm-xv6-intro) | [Discussion](https://www.youtube.com/watch?v=z6dqk6iBBRY) |
| Deadlock<br>OSTEP Ch. 32 | [Part 1](https://youtu.be/Fnp_K63ss44)| | |
| I/O, Disks & Desk Scheduling<br>OSTEP Ch. 36 - 37 | [Part 1](https://youtu.be/SQz2CTpI-NM)<br>[Part 2](https://youtu.be/15dJR01z82k)<br>[Part 3](https://youtu.be/yErUVST4Fv0) | | |
| RAID & File Systems<br>OSTEP Ch. 38 - 39 | [Part 1](https://youtu.be/XF0mKxLrSVs)<br>[Part 2](https://youtu.be/h3WKYo1B19U)<br>[Part 3](https://youtu.be/Mn9g9XWec28)<br>[Part 4](https://youtu.be/EDFoFlzZ8_w) | [xv6 Threads](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/concurrency-xv6-threads) | [Discussion](https://www.youtube.com/watch?v=G9nW9UbkT7s) |
| FS Implementation & FFS<br>OSTEP Ch. 40 - 41 | [Part 1](https://youtu.be/QMjJlCqUYW4)<br>[Part 2](https://youtu.be/87vv7nVdTDA)<br>[Part 3](https://youtu.be/5n0AdNuBObU) | | |
| Journaling<br>OSTEP Ch. 42 | [Part 1](https://youtu.be/piwPJ0sLV0Y)<br>[Part 2](https://youtu.be/MgnQV-ss1wc)<br>[Part 3](https://youtu.be/wwvMNItRyl8) | [MapReduce](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/concurrency-mapreduce) | [Discussion](https://youtu.be/tSiJ_oBSOZE)<br>[Q&A](https://youtu.be/jVmWrr8y0Uw) |
| LFS & SSD<br>OSTEP Ch. 43 - 44 | [Part 1](https://youtu.be/59XSFnXQ-9Q)<br>[Part 2](https://youtu.be/6fbm9u7__L0)<br>[Part 3](https://youtu.be/vvttbstRdj8)<br>["Words of Wisdom"](https://youtu.be/sKTyhqvTUBU) | [File System Checker](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/filesystems-checker) | |

#### OS Extended

The readings are topics not covered in the original Intro to Operating Systems course, but since they're available why not read them? I tried to suplement the readings with projects from other courses.

| Reading | Project |
| --- | ----------- | 
| Distributed Systems<br>OSTEP Ch. 48 | [Distributed Store](http://cs.brown.edu/courses/csci1310/2020/assign/projects/project5.html)|
| AFS & NFS<br>OSTEP Ch. 49 - 50 | [Distributed File System](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/filesystems-distributed) |
| Security<br>OSTEP Ch. 52 - 57 | Couldn't find much outside of a [couple ideas](https://people.eecs.berkeley.edu/~daw/teaching/cs261-f04/projs.html), but nothing structured like the other ones. |

I tried to find projects that had to do with the reading, but there's a couple of challenging projects involving xv6 in MIT's [6.S081: Operating Systems Engineering](https://pdos.csail.mit.edu/6.S081/2020/) such as [network driver](https://pdos.csail.mit.edu/6.S081/2020/labs/net.html).


### The Kernel

To apply my knowledge, I'd like to contribute to the Linux Kernel.

| Reading | Project |
| --- | --- |
| [Linux Kernel Development, 3rd Ed.](https://www.oreilly.com/library/view/linux-kernel-development/9780768696974/) by Robert Love | Contribute to the Linux Kernel... |
| Optionally [Linux Insides](https://0xax.gitbooks.io/linux-insides/content/) | whatever that may look like... | 

### And beyond

I'd eventually like to learn more advanced topics such as Distributed Systems. Remzi has two more courses: [CS-736: Advanced Operating Systems](https://pages.cs.wisc.edu/~remzi/Classes/736/Spring2014/) and [CS-739: Distributed Systems](https://pages.cs.wisc.edu/~remzi/Classes/739/Fall2018/) which are both graduate level courses so it includes a lot of papers *shivers*. However, I came across Columbia's [COMS 4113: Distributed Systems Fundamentals](https://systems.cs.columbia.edu/ds1-class/01-lectures/) which includes some overlap in the Intro OS course but still includes some _fundamental_ information, I may write another post/syllabus about it.
