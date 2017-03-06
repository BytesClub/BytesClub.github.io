---
layout: post
title: Introduction to Git and GitHub
---

> "Real men use the command line"

# Git

Git is a [version control system](https://en.wikipedia.org/wiki/Version_control) to track changes in files in a computer and allow multiple people to work on those files. It was created by [Linus Torvalds](https://www.youtube.com/watch?v=IVpOyKCNZYw) [^ted], in less than 2 weeks.


### Why we need git

Simply put, it is like checkpoints in games, and we can fearlessly modify code, without creating a backup, removing the need to do this:

![copy](/images/git/git-copies.png)

Git is also fully distributive, allowing multiple people to work on a project easily, and maintaining the changes made by them.

![copy](/images/git/vc.png)

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

### Add changes

After modifying/adding files on the repository, to add the changes made to the files in the staging area, use the `git add` command

```
git add <filename>
```

To add all changed files to the staged area, use:

```
git add -A
```

### Creating a checkpoint

Checkpoints in `git` is called a `commit`, and we use the command `git commit`. Basically `git commit` records the changes to the repository.

For a single line commit message, this is used:

```
git commit -m <commit message>
```

### Remotes

The changes in git are made on a local copy of the repository. To communicate this with the outside world, git uses _remotes_. These are the repositories other than the repository on your local disc where you can push the changes made from the local repository. To create a new remote, named _origin_ (it can be any other name) we use:

```
git remote add origin <url>
```

This creates a new remote called `origin` located at `<url>`. Once this is done, we can just write _origin_ in the push command instead of typing the whole URL.

For more explanations, check footnotes [^remote]

### Cloning a repository

Instead of creating a fresh new repository, one may need to work on an already existing repository. For this purpose, cloning a repository comes handy.

```
git clone <remote_url>
```

This helps in creating a local copy of the repository present in `<remote_url>`. In this case, the remotes will automatically be set.

### Branches

Branches in git is used to develop features isolated from each other. Every git repository has a default branch called `master`.

![branch](/images/git/branch.png)

Use other branches at the development stage and merge them to master on completion.

To create a new branch and switch to that branch, use:

```
git checkout -b <branch_name>
```

To switch back to the master branch, use:

```
git checkout master
```

Rather, to switch to any existing branch, use:

```
git checkout <branch_name>
```

To delete an existing branch, 

```
git branch -d <branch_name>
```

### Sending your commits

As of now, all your changes are present in your local repository only. To send these changes to the remote repository, git uses `push`. The syntax of which looks like:

```
git push <remote_name> <branch_name>
```

If you want to send the changes (commits) made on the `master` branch on the remote repository described by the `origin` remote, use:

```
git push origin master
```

### Git Structure

The very basic structure of git looks like the following:

![struct](/images/git/structure.png)

# Github

> Github != git

Github is a company that allows anyone to host their git repositories. Lot's of major open source projects are hosted on GitHub, the most popular (and the most active) being the [Linux Kernel](https://github.com/torvalds/linux). Many well known companies host their open source projects on GitHub like [Google](https://github.com/google), [Facebook](https://github.com/facebook) to just name a few.

### Issues

GitHub has a facility called _issues_, which allows *anyone* to file a bug report, problems related to the project or feature requests related to the project. If you are a developer wishing to contribute to the project, look through the issues and try to fix them. Also, look for the labels in each issue, if you are a beginner or willing to work on something specific.

**But wait!**

You may not have the permission to write on `origin`, what then ?

### Forks

Forking a repository means you have a copy of one repository on your own profile. You will have write access to your forked repository. Push the changes to the forked repository as a remote.

Protip: Do not fork a repository unless you are going to contribute to it

### Pull Requests

To get the original repositories check out your contributions to their project, you need to create a Pull Request. Create a Pull Request to the original repository, describing the changes you have made. The maintainers of the project will review it, and if they are satisfied with the changes, they will merge the Pull Request, and your code will be reflected on the original project.

[^ted]: [The mind behind Linux - Linus Torvalds](https://youtu.be/o8NPllzkFhE)
[^remote]: [What is `git add remote` and `git push origin master`](http://stackoverflow.com/questions/5617211/what-is-git-remote-add-and-git-push-origin-master/5617350#5617350) 

