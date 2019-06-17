# Learning Git and Github

Git is currently the most popular distributed version control system in use in industry today. The concepts are not new, but git in particular has superseded previous tools because it is efficient, works locally and remotely, and best of all, it is open source and maintained by a large community.

If you've never used Git or are still fuzzy on why we need version control, then you should view the following video lessons. From there proceed to the interactive lessons. 

Anytime you setup git for the first time on a computer or virtual machine, you should set some basic configurations as described in the section [One time setup](#one-time-setup)


## Video Lessons

* What is Git and Github? (4min video)
    - [https://www.youtube.com/watch?v=uUuTYDg9XoI](https://www.youtube.com/watch?v=uUuTYDg9XoI)
* Git setup and first time use (8min video)
    - [https://www.youtube.com/watch?v=QqP7YZlZEOo](https://www.youtube.com/watch?v=QqP7YZlZEOo)


## Interactive Git Lessons

* **tryGit:** [https://try.github.io](https://try.github.io)
    - Do this one!
* **Codecademy Learn Git:** [https://www.codecademy.com/learn/learn-git](https://www.codecademy.com/learn/learn-git)


## References
* Git Book
    - [https://git-scm.com/doc](https://git-scm.com/doc)
* Git Command Reference
    - [https://git-scm.com/docs](https://git-scm.com/doc)
* Git and Github resources
    - [https://help.github.com/articles/good-resources-for-learning-git-and-github/](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## Advanced References

The following are resources for advanced usage of Git and Github. You don't have to spend time now (early semester) on this material, but rather, refer back here when you need to.

* The full Codemy School Git Playlist (7 videos)
    - A lot of the advanced topics here, may only make sense once we begin working in groups.
    - [https://www.youtube.com/playlist?list=PLjQo0sojbbxVHcVN4h9DMu6U6spKk21uP](https://www.youtube.com/playlist?list=PLjQo0sojbbxVHcVN4h9DMu6U6spKk21uP)
* Git Workflows (Atlassian Docs)
    - [https://www.atlassian.com/git/tutorials/comparing-workflows/](https://www.atlassian.com/git/tutorials/comparing-workflows/)


## One Time Setup

You should always setup git and let it know who you are. This way the commit log will always have proper author information.

```bash
git config --global user.name "First Last"
git config --global user.email "my@email.com"

git config --global push.default simple
# `input` on mac/linux, `true` on windows
git config --global core.autocrlf input
```

### Explanation of the final two commands
```bash
git config --global push.default simple
```

This tells git to only push updates from your current branch up to remote repositories (like Github). If you don't do this, then the original behavior could be to push all branches, even your experimental ones, up to remote repositories.

```bash
# mac/linux
git config --global core.autocrlf input
# windows only
git config --global core.autocrlf true
```

This setting deals with the end of lines (EOL) in your code files. For the best compatibility across platforms, it is best if windows users set this to `true` and Mac/Linux users set this to `input`.

