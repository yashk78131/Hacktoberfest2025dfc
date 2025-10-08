# Git Workflow Guide for Hacktoberfest Beginners

This guide will help you understand Git and GitHub workflows for contributing to open source projects during Hacktoberfest 2025.

## 📚 Table of Contents

- [Prerequisites](#prerequisites)
- [Basic Git Concepts](#basic-git-concepts)
- [Setting Up Your Environment](#setting-up-your-environment)
- [Complete Contribution Workflow](#complete-contribution-workflow)
- [Common Commands Reference](#common-commands-reference)
- [Troubleshooting Common Issues](#troubleshooting-common-issues)
- [Best Practices](#best-practices)

## Prerequisites

- GitHub account
- Git installed on your computer
- Basic command line knowledge
- Text editor (VS Code, Sublime Text, etc.)

## Basic Git Concepts

### What is Git?
Git is a version control system that tracks changes in files and coordinates work among multiple people.

### Key Terms:
- **Repository (Repo)**: A project folder that contains all files and their version history
- **Fork**: A personal copy of someone else's repository
- **Clone**: Downloading a repository to your local machine
- **Branch**: A parallel version of the main codebase
- **Commit**: A saved snapshot of changes
- **Pull Request (PR)**: A request to merge your changes into the main repository
- **Merge**: Combining changes from different branches

## Setting Up Your Environment

### 1. Install Git
```bash
# Windows (using Git for Windows)
# Download from: https://git-scm.com/download/win

# macOS (using Homebrew)
brew install git

# Linux (Ubuntu/Debian)
sudo apt-get install git
```

### 2. Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 3. Generate SSH Key (Optional but Recommended)
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
# Add the public key to your GitHub account
```

## Complete Contribution Workflow

### Step 1: Fork the Repository
1. Go to the repository on GitHub
2. Click the "Fork" button in the top-right corner
3. This creates a copy in your GitHub account

### Step 2: Clone Your Fork
```bash
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME
```

### Step 3: Add Upstream Remote
```bash
git remote add upstream https://github.com/ORIGINAL_OWNER/REPO_NAME.git
```

### Step 4: Create a New Branch
```bash
git checkout -b feature/your-feature-name
# or
git switch -c feature/your-feature-name
```

### Step 5: Make Your Changes
- Edit files using your preferred text editor
- Test your changes locally
- Follow the project's coding standards

### Step 6: Stage Your Changes
```bash
# Check what files have changed
git status

# Add specific files
git add filename.txt

# Add all changes
git add .

# Add changes interactively
git add -p
```

### Step 7: Commit Your Changes
```bash
git commit -m "Add: brief description of your changes"

# For more detailed commits
git commit -m "Add: feature description

- Detailed explanation of changes
- Why this change was made
- Any additional context"
```

### Step 8: Push to Your Fork
```bash
git push origin feature/your-feature-name
```

### Step 9: Create a Pull Request
1. Go to your fork on GitHub
2. Click "Compare & pull request"
3. Fill out the PR description
4. Submit the pull request

### Step 10: Keep Your Fork Updated
```bash
# Fetch changes from upstream
git fetch upstream

# Switch to main branch
git checkout main

# Merge upstream changes
git merge upstream/main

# Push updates to your fork
git push origin main
```

## Common Commands Reference

### Basic Commands
```bash
# Check status
git status

# View commit history
git log --oneline

# View differences
git diff

# View staged changes
git diff --staged

# Undo changes
git checkout -- filename.txt

# Unstage files
git reset HEAD filename.txt
```

### Branch Management
```bash
# List branches
git branch

# Switch branches
git checkout branch-name
git switch branch-name

# Delete branch
git branch -d branch-name

# Delete remote branch
git push origin --delete branch-name
```

### Remote Management
```bash
# List remotes
git remote -v

# Add remote
git remote add name url

# Remove remote
git remote remove name

# Fetch from remote
git fetch remote-name
```

### Advanced Commands
```bash
# Interactive rebase
git rebase -i HEAD~3

# Cherry-pick commit
git cherry-pick commit-hash

# Stash changes
git stash
git stash pop

# Amend last commit
git commit --amend
```

## Troubleshooting Common Issues

### Issue: "Permission denied (publickey)"
**Solution**: Set up SSH keys or use HTTPS instead
```bash
git clone https://github.com/USERNAME/REPO.git
```

### Issue: "Your branch is behind"
**Solution**: Pull latest changes
```bash
git pull upstream main
```

### Issue: Merge conflicts
**Solution**: Resolve conflicts manually
1. Open conflicted files
2. Choose which changes to keep
3. Remove conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Stage resolved files: `git add filename.txt`
5. Complete merge: `git commit`

### Issue: Wrong commit message
**Solution**: Amend the commit
```bash
git commit --amend -m "Correct message"
```

### Issue: Accidentally committed to main
**Solution**: Create new branch and reset
```bash
git checkout -b feature-branch
git checkout main
git reset --hard HEAD~1
git checkout feature-branch
```

## Best Practices

### Commit Messages
- Use imperative mood: "Add feature" not "Added feature"
- Keep first line under 50 characters
- Use body for detailed explanations
- Reference issues: "Fix #123"

### Branch Naming
- Use descriptive names: `feature/user-authentication`
- Include issue numbers: `fix/issue-456`
- Use prefixes: `feature/`, `fix/`, `docs/`, `test/`

### Code Quality
- Test your changes locally
- Follow project coding standards
- Write clear, readable code
- Add comments for complex logic

### Pull Request Etiquette
- Write clear PR descriptions
- Reference related issues
- Request reviews from maintainers
- Respond to feedback promptly
- Keep PRs focused and small

### Regular Maintenance
- Keep your fork updated
- Delete merged branches
- Clean up old branches
- Sync with upstream regularly

## Additional Resources

- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)
- [GitHub Learning Lab](https://lab.github.com/)
- [First Contributions](https://firstcontributions.github.io/)

## Quick Reference Card

```bash
# Daily workflow
git status                    # Check status
git add .                     # Stage changes
git commit -m "message"       # Commit changes
git push origin branch-name   # Push to GitHub

# Sync with upstream
git fetch upstream           # Get latest changes
git merge upstream/main      # Merge changes
git push origin main         # Update your fork

# Create new feature
git checkout -b feature/name # Create branch
# ... make changes ...
git add .                    # Stage changes
git commit -m "message"      # Commit changes
git push origin feature/name # Push branch
```

---

**Happy Contributing! 🎉**

Remember: Every expert was once a beginner. Don't be afraid to ask questions and learn from the community!
