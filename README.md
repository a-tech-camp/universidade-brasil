# Git

Git is a source control system. It is most often interfaced through its command line interface (cli) of the same name. It can be interfaced with through a website that hosts version controlled repositories (github, gitlab) or through a GUI.

[Documentation](https://git-scm.com/docs/)
[Github Starter Activity](https://guides.github.com/activities/hello-world/)

## 1 High Level Concept
Git trackes changes to a code base or repository. A repository can have many branches that each are the compilation of their own commits. Commits cannot be removed but they can be undone by applying the reverse commit. I can have a master branch that represents code commited to production and have other branches that I am individually working on.


## 2 Getting Started
### 2.1 Installing Git
 - Mac: already included
 - Windows: use [Git Bash](https://gitforwindows.org/)
 - linux: ...? TODO


### 2.2 Cloning repository
Cloning a repository is done once per repository. It will create a folder with the content of that repository.
 - It will also create a `.git` folder within that repository that has information on how to access that repository for the future. Removing this folder will sever that connection

```sh
git clone <repository-address>
```
 - On github the repository address can be copied from a button with the label `Clone or Download`


## 3 Commands
### 3.1 Status
Shows what files are being tracked and have changes
```sh
git status
```

### 3.2 Diff
Shows the changes in tracked files
```sh
git diff
```


### 3.3 Add
Add files to be tracked
```sh
git add . # will add all the files
```
```sh
git add <filename> # will only add a specific file
```

### 3.4 Commit
Commit the current tracked changes (what is displayed after `git diff`) to a single commit
```sh
git commit -m '<message>' # where message is the commits message
```

### 3.5 Push
Push the code from your local instance of the remote repository at the hosting site
```sh
git push
```

### 3.7 Branch
List all branches or create a branch
```sh
git branch # will list all branches
```

```sh
git branch <branch-name> # create a branch with the name <branch-name>
```
 - creating a branch will explicitly create the branch at the ccommit you are at. 
 - This will not change your code only where you add your changes. 
 - It is likely that you will want to check what branch you are on and make sure it is up to date

### 3.8 Checkout
checkout a branch or a file in a branch
```sh
git checkout <branch-name>
```

You can create a branch at the same time as checkout out, with a `-b` flag
```sh
git checkout -b <branch-name>
```

### 3.9 Merge
Merging is ussed to combine branches. 
```sh
git merge <branch-name>
```
 - where `<branch-name>` is what I'd like to merge


Often times both branches are ahead of where they were at the time of branching. It's a good technique to merge in a master branch while on your branch
```
git checkout <branch-name>
git merge master
```
 - this can often lead to conflicts
 - your repository will be in a state where it has both set of changes sepereated by `==================` 

The most common strategy is to keep our changes on conflicts
```sh
git checkout <branch-name>
git merge master -s ours
```

If you'd like to referenece the master that is at origin (hosted on the cloud)
```sh
git checkout <branch-name>
git merge master -s ours
```
