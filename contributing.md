---
layout: page
title: Contribution
---

### Adding a repository

If you wish to add a repository in the organisation, write about the project details at [bytes-club@googlegroups.com](mailto:bytes-club@googlegroups.com) or drop a message about the repository on the gitter channel [#Bytes_Club/General](https://gitter.im/Bytes_Club/General).

---

### For Beginners

* Please read [The Beginner's Guide](/2017/02/18/introducing-bytesclub/)
* Introduce yourself by sending a mail to the mailing list ( [bytes-club@googlegroups.com](mailto:bytes-club@googlegroups.com) ), providing your past experiences. We surely have something for you.
* If you are a beginner and don't know where to start, head over to the [Github page of the organisation](https://github.com/BytesClub), and look for a project which you are interested in.
* Setup the project by following the Documentation on your local machine (usually the `README` file).

#### Creating issues
* If you find any issues/feature enhancement regarding any project, go to the issues tab and create an issue regarding it.


##### Solving an issue
* Go to the issues tab, and look for the issues which interests you. If you are a beginner, look for the label `dificulty/easy` to start with.
* Work on the issue by forking the repository in your account, work on the issue and create a Pull Request regarding the same. For more details, read the [tips for contributing](#tips-for-contribution)

In case you face any kind of trouble, feel free to ask in the gitter channel [#Bytes_Club/General](https://gitter.im/Bytes_Club/General).

---

### Tips for Contribution

* Create a new branch while working on an issue.
* Use proper commit messages. A typical commit message should look like this: 

```
shortlog: commit message

commit body

fixes #<issue_number>

Signed-off-by: [Your name] <your email>
```

where short log is the area/filename where you are making the change. Also, in order to avoid writting the signoff manually, add the `--signoff` flag while committing. Thus the full command should be:

```
git commit --signoff
```

Keep in mind the following points while writting a commit message

    - Separate subject from body with a blank line
    - Limit the subject line to 50 characters
    - Capitalize the subject line
    - Do not end the subject line with a period
    - Use the imperative mood in the subject line
    - Wrap the body at 72 characters
    - Use the body to explain what and why vs. how

For more information about proper commit messages, read [this](https://chris.beams.io/posts/git-commit/).

To add this by default, download the [commit message template](https://gist.githubusercontent.com/RudraNilBasu/afa9f64f9b7323e2c6e3476c4a8b7ddd/raw/83475f2c5f2ae6788bfae083bf2078b464483cbc/git_commit_message.txt), and run

```
$ git config --global commit.template /path/to/file
```

before committing.

### Coding Conventions

We follow [the Linux Kernel's coding convention]({{ site.baseurl }}/docs/coding_style.pdf).

-----

More about git [here](/docs/git.pptx)
