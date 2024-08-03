---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - git
Creation Date: 
Last Date: 
References: 
description: Tools -> Git -> Command Cheat Sheet
---

## Basic Commands

### Initialize a new Git repository
```sh
git init
```

### Clone an existing repository
```sh
git clone <repository-url>
```

### Check the status of your repository
```sh
git status
```

### Add files to the staging area
```sh
git add <file>
```

### Commit changes
```sh
git commit -m "commit message"
```

### Push changes to a remote repository
```sh
git push
```

### Pull changes from a remote repository
```sh
git pull
```

## Branching

### List all branches
```sh
git branch
```

### Create a new branch
```sh
git branch <branch-name>
```

### Switch to a different branch
```sh
git checkout <branch-name>
```

### Create and switch to a new branch
```sh
git checkout -b <branch-name>
```

### Merge a branch into the current branch
```sh
git merge <branch-name>
```

## Remote Repositories

### Add a remote repository
```sh
git remote add <remote-name> <repository-url>
```

### Remove a remote repository
```sh
git remote remove <remote-name>
```

### Show remote repositories
```sh
git remote -v
```

## Stashing

### Stash changes
```sh
git stash
```

### Apply stashed changes
```sh
git stash apply
```

### List stashed changes
```sh
git stash list
```

## Undoing Changes

### Unstage a file
```sh
git reset <file>
```

### Revert a commit
```sh
git revert <commit-id>
```

### Reset to a previous commit
```sh
git reset --hard <commit-id>
```

## Viewing History

### Show commit history
```sh
git log
```

### Show a specific commit
```sh
git show <commit-id>
```

### Show changes
```sh
git diff
```

## Tagging

### Create a new tag
```sh
git tag <tag-name>
```

### List all tags
```sh
git tag
```

### Push tags to remote
```sh
git push --tags
```