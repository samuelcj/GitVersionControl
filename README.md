# Learning Git and GitHub

This repository is a comprehensive guide to learning and practicing Git and GitHub. It contains useful Git commands with their explanations and examples for efficient version control and collaboration.

## Table of Contents

1. [Setting Up Git](#setting-up-git)
2. [Working with Repositories](#working-with-repositories)
3. [Branch Management](#branch-management)
4. [Staging, Committing, and Logging](#staging-committing-and-logging)
5. [Merge and Rebase](#merge-and-rebase)
6. [Undoing Changes](#undoing-changes)
7. [Working with Remote Repositories](#working-with-remote-repositories)
8. [Submodules](#submodules)
9. [Advanced Features](#advanced-features)

---

## Setting Up Git

1. **Create RSA key pair:**
   ```bash
   ssh-keygen -t rsa -b 2048 -C "<comment>"
   ```

2. **Configure username:**
   ```bash
   git config --global user.name "<Your Name>"
   ```

## Working with Repositories

1. **Clone a repository via SSH:**
   ```bash
   git clone git@gitlab.com:<username>/<repo-name>
   ```

2. **Clone a repository via HTTP with token:**
   ```bash
   git clone https://<username>:<authentication-token>@github.com/<repo-name>.git
   ```

3. **Initialize a new local repository:**
   ```bash
   git init
   ```

4. **Add a remote repository:**
   ```bash
   git remote add origin <remote-repo-URL>
   ```

5. **Check connected remote repositories:**
   ```bash
   git remote get-url origin
   ```

## Branch Management

1. **Create or rename a branch:**
   ```bash
   git branch -m <branch-name>
   ```

2. **Delete a branch:**
   ```bash
   git branch -d <branch-name>
   ```

3. **Change branch:**
   ```bash
   git branch -M main
   ```

## Staging, Committing, and Logging

1. **Stage changes:**
   ```bash
   git add <file-name> | git add . | git add -A
   ```

2. **Commit changes:**
   ```bash
   git commit -m "<commit-message>"
   ```

3. **Amend a commit:**
   ```bash
   git commit --amend
   ```

4. **View commit history:**
   ```bash
   git log
   ```

5. **Go back to a specific commit:**
   ```bash
   git checkout <commit-hash>
   ```

## Merge and Rebase

1. **Merge branches:**
   ```bash
   git merge <source-branch>
   ```

2. **Rebase a branch:**
   ```bash
   git push -r
   ```

3. **Continue rebase after resolving conflicts:**
   ```bash
   git rebase --continue
   ```

4. **Abort rebase:**
   ```bash
   git rebase --abort
   ```

## Undoing Changes

1. **Remove a tracked file:**
   ```bash
   git rm --cached <file-name>
   ```

2. **Reset to a previous commit (discard changes):**
   ```bash
   git reset --hard HEAD~1
   ```

3. **Reset to a previous commit (keep changes):**
   ```bash
   git reset --soft HEAD~1
   ```

4. **Revert a commit:**
   ```bash
   git revert <commit-hash>
   ```

## Working with Remote Repositories

1. **Push changes to a remote repository:**
   ```bash
   git push
   ```

2. **Set upstream for a branch:**
   ```bash
   git push --set-upstream origin <branch-name>
   ```

3. **Force push changes:**
   ```bash
   git push --force
   ```

## Submodules

1. **Add a submodule to a repository:**
   ```bash
   git submodule add <submodule-URL> <submodule-name>
   ```

## Advanced Features

1. **Using `.gitignore` to exclude files or directories:**
   - Example of `.gitignore` content:
     ```
     /node_modules
     .env
     build/*
     ```

2. **Stashing changes:**
   ```bash
   git stash        # Save work in progress
   git stash pop    # Retrieve stashed changes
   ```

3. **Working with merge conflicts:**
   - After resolving conflicts, mark them resolved:
     ```bash
     git add <conflicted-file>
     git rebase --continue
     ```

---

### Contributions
Feel free to contribute additional commands or suggestions to improve this guide!


