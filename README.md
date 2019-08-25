# Mercurial VS Git

This little documentation, I am going to compare Mercurial line comands and Git command in common workflows. In any case, to go deeper in this technologies, i recommend you to check the oficial documentation.

# Simple workflow comparation

## Starting from scratch
### Mercurial
	hg init

### Git
	git init
  
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
	
# Removing commands

## Revert all changes
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

## Uncommit changes
### Mercurial
	hg strip [OPTIONS]

### Git
	git reset [OPTIONS]
