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