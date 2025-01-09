---
title: "Git Cheatsheet: Essential Commands and Their Usage"
datePublished: Mon Jan 06 2025 15:33:43 GMT+0000 (Coordinated Universal Time)
cuid: cm5l7bw9k000b09kzfgw9c3o0
slug: git-cheatsheet
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1736177611568/51385fd5-3ccc-4fc1-904a-3538b56dd857.jpeg
tags: github, git, github-actions-1, git-commands, gitcheatsheet

---

Git is an essential tool for modern software development, enabling efficient version control, collaboration, and automation. Whether you're just starting with Git or looking to streamline your workflows, having a quick reference can make a huge difference. This Git cheatsheet provides a concise overview of the most commonly used Git commands and concepts. From managing repositories and branches to handling commits and merges, this guide is designed to help developers navigate Git with ease. Whether you're working solo or as part of a team, this cheatsheet will serve as a handy resource to improve your Git proficiency and boost productivity.

## Getting Started

### Configure Git

```bash
# Set your username
git config --global user.name "Your Name"

# Set your email
git config --global user.email "youremail@example.com"

# Check configuration
git config --list
```

### Initialize and Clone

```bash
# Initialize a new Git repository
git init

# Clone an existing repository
git clone <repository_url>
```

## Working with Changes

### Check Repository Status

```bash
# Show the status of your working directory
git status
```

### Staging Changes

```bash
# Add a specific file to the staging area
git add <file>

# Add all changes in the working directory to staging
git add .
```

### Committing Changes

```bash
# Commit staged changes with a message
git commit -m "Commit message"

# Commit with a detailed message editor
git commit
```

### Viewing History

```bash
# Show commit history
git log

# Show a concise commit history
git log --oneline

# Show changes in a specific commit
git show <commit_hash>
```

## Branching and Merging

### Working with Branches

```bash
# List all branches
git branch

# Create a new branch
git branch <branch_name>

# Switch to a branch
git checkout <branch_name>

# Create and switch to a new branch
git checkout -b <branch_name>
```

### Merging Branches

```bash
# Merge a branch into the current branch
git merge <branch_name>
```

### Deleting Branches

```bash
# Delete a local branch
git branch -d <branch_name>

# Force delete a branch
git branch -D <branch_name>
```

## Working with Remote Repositories

### Adding and Fetching Remotes

```bash
# Add a remote repository
git remote add origin <repository_url>

# Fetch updates from the remote repository
git fetch origin
```

### Pushing Changes

```bash
# Push changes to the remote repository
git push origin <branch_name>

# Set upstream for the branch and push
git push -u origin <branch_name>
```

### Pulling Changes

```bash
# Fetch and merge changes from the remote repository
git pull origin <branch_name>
```

## Undoing Changes

### Unstaging Changes

```bash
# Unstage a file
git reset <file>
```

### Reverting Commits

```bash
# Create a new commit that reverts a previous one
git revert <commit_hash>
```

### Resetting to a Previous State

```bash
# Reset to a previous commit (keep changes in working directory)
git reset --soft <commit_hash>

# Reset to a previous commit (discard changes in working directory)
git reset --hard <commit_hash>
```

## Stashing Changes

```bash
# Stash changes
git stash

# List stashes
git stash list

# Apply the most recent stash
git stash apply

# Drop the most recent stash
git stash drop
```

## Tagging

```bash
# Create a new tag
git tag <tag_name>

# Create an annotated tag
git tag -a <tag_name> -m "Tag message"

# Push tags to the remote repository
git push origin --tags
```

## Tips and Tricks

### Show Differences

```bash
# Show changes in the working directory
git diff

# Show staged changes
git diff --staged
```

### Clean Up Untracked Files

```bash
# Remove untracked files
git clean -f
```

This cheatsheet covers the most commonly used Git commands to help you manage your repositories effectively. Master these commands, and you'll have a solid foundation for working with Git in any project! Also do checkout the article below to get more insights on Git.

%[https://asbk.hashnode.dev/git-for-devops]