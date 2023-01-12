# FML

## Fundamentals of Machine Learning - course notes, code and auxiliary material

#### Purpose

Use to store and track Jupyter notebooks and other core material. 



#### Binder

Use these notebooks on <mybinder.org>...

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/variationalform/FML.git/HEAD)



#### Git - usage notes

This repo was originally set up on git hub and then, locally,

```bash
cd /to/parent/directory
git clone git@github.com:variationalform/FML.git
```

Then, for example, 
```bash
cd FML
git add notebooks/*
git add *
git add .gitignore 
git reset    # to undo and start again
git status
git commit -m 'Initial commit for notebooks'
git push
```
Note that `.gitignore` is a hidden file. It's worth collaborating with it though.

From <https://stackoverflow.com/questions/54825213/git-log-source-in-pretty-format>

```bash
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```


If changes are made remotely, sync them locally and see what changed with,

```bash
git pull            # changes the lovcal branch
git fetch           # doesn't change local branch, just remote
git log --patch     # see what changed
git whatchanged     # deprecated
git log --pretty=oneline
git log --pretty=short
git log --pretty=medium
git log --pretty=full
git log --pretty=fuller
```

If changes are made in a pulled branch (e.g. by <https://github.com/xiaochuany>, try this:

```bash
# Step 1: From your project repository, check out a new branch and test the changes.

git checkout -b xiaochuany-main main
git pull https://github.com/xiaochuany/FML.git main

# Step 2: Merge the changes and update on GitHub.

git checkout main
git merge --no-ff xiaochuany-main
git push origin main
```
