---
title: Self Taught Operating Systems
date: 2022-01-12T02:05:09.972Z
draft: true
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
| Intro & Processes<br>OSTEP Ch. Pre - 6 | <ul><li>[Part 1](https://www.youtube.com/watch?v=3uMbb9dLtlE)</li><li>[Part 2](https://www.youtube.com/watch?v=K4qbAiC77Yo)</li><li>[Part 3](https://www.youtube.com/watch?v=LVxN7ZkGh3w)</li></ul> | [Unix Utilities](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/initial-utilities) | [Discussion](https://www.youtube.com/watch?v=rgcq9x8LtGQ) |
| Scheduling<br>OSTEP Ch. 7 - 9 | <ul><li>[Part 1](https://www.youtube.com/watch?v=oTd72Yp2m8w)</li><li>[Part 2](https://www.youtube.com/watch?v=Q09UgVfragU)</li><li>[Part 3](https://www.youtube.com/watch?v=fin5-82L-r8)</li></ul> |
| Memory Management & Paging<br>OSTEP Ch. 13 - 16; 18 | <ul><li>[Part 1](https://youtu.be/cAiwISFta4g)</li><li>[Part 2](https://youtu.be/I0RIlSN0DzM)</li><li>[Part 3](https://youtu.be/0WVoWlOT-kY)</li></ul> | [Intro To Kernel Hacking](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/initial-xv6) | [Discussion](https://www.youtube.com/watch?v=vR6z2QGcoo8) |
| Paging: TLB & Paging: Smaller<br>OSTEP Ch. 19 - 20 | <ul><li>[Part 1](https://youtu.be/wAx_h3HkIX0)</li><li>[Part 2](https://youtu.be/7BOXM2XgGO4)</li><li>[Part 3](https://youtu.be/LprKOBsALGA)</li></ul> | [Unix Shell](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/processes-shell) | [Discussion](https://youtu.be/76PfvXTwF04) |
| Beyond Physical Memory<br>OSTEP Ch. 21 - 22 | <ul><li>[Part 1](https://youtu.be/wAx_h3HkIX0)</li><li>[Part 2](https://youtu.be/7BOXM2XgGO4)</li><li>[Part 3](https://youtu.be/LprKOBsALGA)</li></ul> | 
| Threads & Locks<br>OSTEP Ch. 25 - 26; 28 | <ul><li>[Part 1](https://www.youtube.com/watch?v=ggPkFxOTwHY)</li><li>[Part 2](https://www.youtube.com/watch?v=4tPXkN5nRQs)</li></ul> | [xv6 Lottery Scheduler](https://github.com/remzi-arpacidusseau/ostep-projects/tree/master/scheduling-xv6-lottery) | [Discussion](https://www.youtube.com/watch?v=eYfeOT1QYmg) |
| Locks, CVs & More CVs<br>OSTEP Ch. 29 - 30 | <ul><li>[Part 1](https://www.youtube.com/watch?v=4PghlMdp9cU)</li><li>[Part 2](https://www.youtube.com/watch?v=hivv8F-LjzY)</li><li>[Part 3](https://youtu.be/BoLYvNp2Lc4)</li></ul> |
| Semaphores<br>OSTEP Ch. 31 | | | |
| Deadlock<br>OSTEP Ch. 32 | | | |
| I/O, Disks & Desk Scheduling<br>OSTEP Ch. 36 - 37 | | | |
| RAID & File Systems<br>OSTEP Ch. 38 - 39 | | | |
| FS Implementation & FFS<br>OSTEP Ch. 40 - 41 | | | |
| Journaling<br>OSTEP Ch. 42 | | | |
| LFS & SSD<br>OSTEP Ch. 43 - 44 | | | |

#### OS Extended

| Reading | Lectures | Project | Discussion |
| --- | ----------- | --- | --- | --- |
| Distributed Systems<br>OSTEP Ch. 48 | 
| AFS & NFS<br>OSTEP Ch. 49 - 50 | 
| Security<br>OSTEP Ch. 52 - 57 |

### The Kernel

To apply my knowledge, I'd like to contribute to the Linux Kernel.

| Reading | Project |
| --- | --- |
| [Linux Kernel Development, 3rd Ed.](https://www.oreilly.com/library/view/linux-kernel-development/9780768696974/) by Robert Love | Contribute to the Linux Kernel... |
| Optionally [Linux Insides](https://0xax.gitbooks.io/linux-insides/content/) | whatever that may look like... | 

### And beyond

I'd eventually like to learn more advanced topics such as Distributed Systems. Remzi has two more courses: [CS-736: Advanced Operating Systems](https://pages.cs.wisc.edu/~remzi/Classes/736/Spring2014/) and [CS-739: Distributed Systems](https://pages.cs.wisc.edu/~remzi/Classes/739/Fall2018/) which are both graduate level courses so it includes a lot of papers *shivers*. However, I came across Columbia's [COMS 4113: Distributed Systems Fundamentals](https://systems.cs.columbia.edu/ds1-class/01-lectures/) which includes some overlap in the Intro OS course but still includes some _fundamental_ information, I may write another post/syllabus about it.
