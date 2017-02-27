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

### Remotes

The changes in git are made on a local copy of the repository. To communicate this with the outside world, git uses _remotes_. These are the repositories other than the repository on your local disc where you can push the changes made from the local repository. To create a new remote, named _origin_ (it can be any other name) we use:

```
git remote add origin <url>
```

This creates a new remote called `origin` located at `<url>`. Once this is done, we can just write _origin_ in the push command instead of typing the whole URL.

For more explanations, check footnotes [^remote]

[^ted]: [The mind behind Linux - Linus Torvalds](https://youtu.be/o8NPllzkFhE)
[^remote]: [What is `git add remote` and `git push origin master`](http://stackoverflow.com/questions/5617211/what-is-git-remote-add-and-git-push-origin-master/5617350#5617350) 

