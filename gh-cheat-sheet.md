# GitHub Beginners Cheat Sheet

## Setup

### Install Git
To install Git, follow the instructions for your operating system. Here are some links:
- **Windows**: [Git for Windows](https://gitforwindows.org/)  
- **macOS**: Install via [Homebrew](https://brew.sh/)
   ```bash
   brew install git
   ```  
- **Linux**: Use package managers, e.g.,  
   ```bash
   sudo apt-get install git  # Debian/Ubuntu
   sudo dnf install git      # Fedora
   ```  

### Configure Name/Email
Set up your name and email in Git:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Creating a Repo
To create a new repository:
1. Go to GitHub and click on `New`.
2. Fill out the repository name, description, and other options.
3. Click `Create repository`.

## Cloning
To clone a repository:
```bash
git clone https://github.com/username/repo.git
```

## Status/Add/Commit
To check the status of your repo:
```bash
git status
```

To stage files for commit:
```bash
git add filename
```

To commit changes:
```bash
git commit -m "Commit message"
```

## Branching
### Create
To create a new branch:
```bash
git branch branch-name
```

### Switch
To switch branches:
```bash
git checkout branch-name
```

### Merge
To merge a branch into the current branch:
```bash
git merge branch-name
```

## Push/Pull
To push changes to the remote repository:
```bash
git push origin branch-name
```

To pull changes from the remote repository:
```bash
git pull origin branch-name
```

## Remotes
To view your remotes:
```bash
git remote -v
```

To add a remote:
```bash
git remote add origin https://github.com/username/repo.git
```

## .gitignore Basics
A `.gitignore` file tells Git which files to ignore.
Example:
```
# Ignore node_modules
node_modules/

# Ignore environment files
.env
```

## Undo (Restore/Reset/Revert)
To reset a file to the last commit:
```bash
git restore filename
```

To unstage a file:
```bash
git reset filename
```

To revert a commit:
```bash
git revert commit-id
```

## Stashing
To stash your changes:
```bash
git stash
```

To apply the stashed changes:
```bash
git stash apply
```

## Logs/Diffs
To view commit logs:
```bash
git log
```

To view differences:
```bash
git diff
```

## Tags
To create a new tag:
```bash
git tag -a v1.0 -m "Version 1.0"
```

## GitHub Flow with PRs
1. **Fork** the repository.
2. **Branch** off from the main branch.
   ```bash
git checkout -b new-feature
```
3. **Commit** your changes.
4. **Push** your branch to the remote.
   ```bash
git push origin new-feature
```
5. **Open a Pull Request** on GitHub.
6. **Review** changes and address feedback.
7. **Merge** the PR once approved.

## Issues
To create a new issue:
1. Go to `Issues` tab in your repository.
2. Click `New Issue` and fill out the details.

## Releases
To create a new release:
1. Go to `Releases` tab.
2. Click `Draft a new release` and fill in the version details.

## Useful Commands
```bash
git --version  # Check Git version
git help        # Get help
```

---

This cheat sheet covers the essentials for beginners to get started with Git and GitHub!