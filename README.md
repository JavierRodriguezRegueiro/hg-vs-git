# Mercurial VS Git

This little documentation, I am going to compare Mercurial line comands and Git command in common workflows. In any case, to go deeper in this technologies, i recommend you to check the oficial documentation.

- [Git](https://git-scm.com/docs)
- [Mercurial](https://www.mercurial-scm.org/guide)

# Sections
- [list of my commonly used Git commands](#list-of-my-commonly-used-Git-commands)
- [Simple workflow comparation](#simple-workflow-comparation)
	- [Starting from scratch](#starting-from-scratch)
	- [Configuring](#configuring)
	- [Adding changes](#adding-changes)
	- [Check differences](#check-differences)
	- [Check status](#check-status)
	- [Commit changes](#commit-changes)
	- [Check workspace log](#check-workspace-log)
	- [Push commits](#push-commits)
- [Removing commands](#removing-commands)
	- [Revert all uncommit changes](#revert-all-uncommit-changes)
	- [Remove file](#remove-file)
	- [Remove commit](#remove-commit)
	


# List of my commonly used Git commands

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |




# Simple workflow comparation

## Starting from scratch
### Mercurial
	hg init

### Git
	git init
  
## Configuring
### Mercurial
To configure in mercurial, you need to modify your .hgrc file.
### Git
	git remote add <name> <url> # Adding a remote repository
	git config --global user.name "FIRST_NAME LAST_NAME" # Adding name
	git config --global user.email "MY_NAME@example.com" # Adding email
	

## Adding changes
### Mercurial
	hg add

### Git
	git add
> **Note:** In mercurial, this command is just necessary when you want to add a new file in your workspace, but in git you need to use it if you want to add modification in any file too

## Check differences
### Mercurial
	hg diff

### Git
	git diff

## Check status
### Mercurial
	hg status

### Git
	git status

## Commit changes
### Mercurial
	hg commit

### Git
	git commit
  
## Check workspace log
### Mercurial
	hg log

### Git
	git log
	
## Push commits
### Mercurial
	hg push [OPTIONS]

### Git
	git push <remote-repository> <branch-name> [OPTIONS]
	
# Removing commands

## Revert all uncommit changes
### Mercurial
	hg revert -a [OPTIONS]

### Git
	git checkout .
	
## Remove file
### Mercurial
	hg remove [OPTIONS] <file>
> **Note:** If you do not want to remove the file from disc, use **hg** **forget**

### Git
	git rm [OPTIONS] <file>
> **Note:** If you do not want to remove the file from disc, use **hg** **forget** **git** **rm** **--cached** **file**

## Remove commit
### Mercurial
	hg strip [OPTIONS]

### Git
	git reset [OPTIONS]
