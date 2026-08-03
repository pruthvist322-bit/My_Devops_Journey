# Day 32 – Introduction to Git & GitHub

## Overview

Today I started learning one of the core tools used in DevOps: **Git and GitHub**.

I learned how Git helps in version control and how GitHub is used to host repositories for collaboration and code management. I also performed hands-on practice by connecting my EC2 instance and IDE to GitHub, creating branches, committing changes, and merging them.

---

## What is Git?

Git is a **Distributed Version Control System (DVCS)** that helps developers track changes in source code, collaborate with team members, and maintain different versions of a project.

---

## What is GitHub?

GitHub is a **cloud-based platform** that hosts Git repositories. It provides collaboration features such as pull requests, code reviews, issue tracking, and repository management.

---

## Difference Between Git and GitHub

### Git
- Version Control System
- Works locally on the machine
- Tracks code changes
- Doesn't require an internet connection for most operations

### GitHub
- Cloud-based repository hosting platform
- Stores Git repositories online
- Enables collaboration among developers
- Requires an internet connection

---

## Connecting EC2 Instance with GitHub

Learned how to:

- Install Git on an EC2 instance
- Configure Git
- Connect the EC2 instance with a GitHub repository
- Clone repositories
- Push and pull code changes

---

## Connecting GitHub Repository with VS Code

Learned how to connect a GitHub repository using Visual Studio Code.

Steps performed:

- Installed Git
- Opened the project in VS Code
- Connected the repository
- Initialized Git
- Published the repository
- Synced changes with GitHub

---

## Connecting GitHub Using Command Prompt

Learned how to use Git through the terminal.

Practiced common Git commands for managing repositories.

---

## Common Git Commands Practiced

Initialize Git Repository

```bash
git init
```

Clone Repository

```bash
git clone <repository-url>
```

Check Status

```bash
git status
```

Add Files

```bash
git add .
```

Commit Changes

```bash
git commit -m "Commit Message"
```

Push Changes

```bash
git push origin main
```

Pull Latest Changes

```bash
git pull origin main
```

Create a Branch

```bash
git branch branch-name
```

Switch Branch

```bash
git checkout branch-name
```

Merge Branch

```bash
git merge branch-name
```

---

## Git Merge vs Git Rebase vs Git Squash

### Git Merge

- Combines two branches
- Preserves complete commit history
- Creates a Merge Commit

**Advantages**
- Easy to understand
- Maintains history

**Disadvantages**
- Commit history can become complex

---

### Git Rebase

- Moves commits from one branch onto another
- Creates a cleaner commit history

**Advantages**
- Linear project history
- Cleaner commit log

**Disadvantages**
- Should be avoided on shared branches

---

### Git Squash

- Combines multiple commits into a single commit

**Advantages**
- Cleaner commit history
- Easier to review code

**Disadvantages**
- Individual commit history is lost

---

## Hands-on Activity

- Created a GitHub Repository
- Connected the repository with VS Code
- Connected the repository using the terminal
- Connected EC2 Instance with GitHub
- Added project files
- Created a new branch
- Committed changes
- Merged the branch into the main branch
- Practiced Git commands using both Terminal and VS Code

---

## VS Code Extensions Explored

Learned about useful Git and GitHub extensions in Visual Studio Code that improve productivity and simplify source code management.

---

## What I Learned

- What is Git
- What is GitHub
- Difference between Git and GitHub
- Connecting EC2 with GitHub
- Connecting GitHub with VS Code
- Connecting GitHub using Terminal
- Common Git Commands
- Git Merge
- Git Rebase
- Git Squash
- Hands-on Branching and Merging
- Useful VS Code Extensions for Git

---

## Key Takeaway

Git is the foundation of version control, while GitHub enables collaboration and repository management. Understanding branching, merging, rebasing, and Git workflows is an essential skill for every DevOps Engineer.

---

