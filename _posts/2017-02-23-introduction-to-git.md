---
layout: post
title: Introduction to Git
---

Git is a [version control system](https://en.wikipedia.org/wiki/Version_control) to track changes in files in a computer and allow multiple people to work on those files. It was created by [Linus Torvalds](https://www.youtube.com/watch?v=IVpOyKCNZYw) [^ted], in less than 2 weeks.


### Why we need git

Simply put, it is like checkpoints in games, and we can fearlessly modify code, without creating a backup, removing the need to do this:

![copy](/images/git/git-copies.png)

### Installing git

Git is installed on Debian/Ubuntu, from the package manager by:

```
sudo apt-get install git
```

### Create a git repository

To create a new git repository, create a new directory, go to the directory via the terminal, and perform a

```
git init
```
to create a new git repository

[^ted]: [The mind behind Linux - Linus Torvalds](https://youtu.be/o8NPllzkFhE)


