# Mercurial VS Git

This little documentation, I am going to compare Mercurial line comands and Git command in common workflows. In any case, to go deeper in this technologies, i recommend you to check the oficial documentation.

- [Git](https://git-scm.com/docs)
- [Mercurial](https://www.mercurial-scm.org/guide)

# Sections
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
