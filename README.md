# FML

## Fundamentals of Machine Learning - course notes, code and auxiliary material

#### Purpose

Use to store and track Jupyter notebooks and other core material. 

#### Licencing

GPL 3.0 applies by default to all files on this repository that do not explicitly 
claim their own licence (e.g. Creative Commons).



#### Binder

Use these notebooks on <https://mybinder.org/v2/gh/variationalform/FML.git/HEAD>...

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
git log -p
git log --oneline
```
Note that `.gitignore` is a hidden file. It's worth collaborating with it though.

From <https://stackoverflow.com/questions/54825213/git-log-source-in-pretty-format>,
this is a stylised log output.

```bash
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

#### Some More Useful Stuff

```bash
jupyter notebook list # obtain the notebook token if it gets requested.
git reflog
git fetch && git diff main origin/main
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

Creating a presentation from a jupyter notebook:

```bash
in the notebook select
view -> cell Toolbar -> slideshow
For each cell select slide type

Then:
# command to convert notebook to presentation
jupyter nbconvert --to slides presentation.ipynb

In the browser do this...
file:///home/.../presentation.slides.html?print-pdf#/

which will then be available to save as PDF.

```

Main reference for the above was 
<https://mljar.com/blog/jupyter-notebook-presentation/>

