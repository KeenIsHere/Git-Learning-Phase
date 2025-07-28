# 🚀 Git Commands Reference Guide

A comprehensive guide to essential Git commands every developer should know when starting a new project or managing existing repositories.

## 📋 Table of Contents
- [Initial Setup](#-initial-setup)
- [Creating a New Repository](#-creating-a-new-repository)
- [Adding an Existing Project](#-adding-an-existing-project-to-git)
- [Basic Workflow Commands](#-basic-workflow-commands)
- [Branch Management](#-branch-management)
- [Remote Repository Operations](#-remote-repository-operations)
- [Viewing History and Changes](#-viewing-history-and-changes)
- [Undoing Changes](#-undoing-changes)
- [Best Practices](#-best-practices)

---

## ⚙️ Initial Setup

Configure Git with your identity (run once per machine):

```bash
# Set your name and email globally
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check your configuration
git config --list

# Set default branch name to 'main'
git config --global init.defaultBranch main
```

---

## 🆕 Creating a New Repository

### Option 1: Start from scratch locally
```bash
# Create and navigate to your project directory
mkdir my-new-project
cd my-new-project

# Initialize Git repository
git init

# Create initial files
touch README.md
echo "# My New Project" > README.md

# Add and commit initial files
git add .
git commit -m "🎉 Initial commit"
```

### Option 2: Clone from remote repository
```bash
# Clone a repository
git clone https://github.com/username/repository-name.git
cd repository-name
```

---

## 📁 Adding an Existing Project to Git

If you have an existing project folder without Git:

```bash
# Navigate to your existing project
cd /path/to/your/existing-project

# Initialize Git repository
git init

# Add all files to staging area
git add .

# Create initial commit
git commit -m "🎉 Initial commit - Add existing project files"

# Add remote repository (if you have one)
git remote add origin https://github.com/username/your-repo.git

# Push to remote repository
git branch -M main
git push -u origin main
```

---

## 🔄 Basic Workflow Commands

### Checking Status and Adding Files
```bash
# Check repository status
git status

# Add specific file to staging area
git add filename.txt

# Add all files to staging area
git add .

# Add all files with specific extension
git add *.js

# Remove file from staging area
git reset filename.txt
```

### Committing Changes
```bash
# Commit with message
git commit -m "✨ Add new feature"

# Commit with detailed message
git commit -m "🐛 Fix login bug

- Fixed authentication issue
- Updated error handling
- Added input validation"

# Add and commit in one command
git commit -am "📝 Update documentation"
```

### Common Commit Message Emojis
- 🎉 `:tada:` - Initial commit
- ✨ `:sparkles:` - New feature
- 🐛 `:bug:` - Bug fix
- 📝 `:memo:` - Documentation
- 🎨 `:art:` - Code structure/format
- ⚡ `:zap:` - Performance improvement
- 🔧 `:wrench:` - Configuration changes
- 🚀 `:rocket:` - Deployment

---

## 🌳 Branch Management

```bash
# List all branches
git branch

# Create new branch
git branch feature-name

# Create and switch to new branch
git checkout -b feature-name
# or (newer syntax)
git switch -c feature-name

# Switch to existing branch
git checkout branch-name
# or
git switch branch-name

# Merge branch into current branch
git merge feature-name

# Delete branch (after merging)
git branch -d feature-name

# Delete branch (force delete)
git branch -D feature-name
```

---

## 🌐 Remote Repository Operations

```bash
# List remote repositories
git remote -v

# Add remote repository
git remote add origin https://github.com/username/repo.git

# Change remote URL
git remote set-url origin https://github.com/username/new-repo.git

# Fetch changes from remote
git fetch origin

# Pull changes from remote
git pull origin main

# Push changes to remote
git push origin main

# Push and set upstream branch
git push -u origin main

# Push all branches
git push --all origin
```

---

## 👀 Viewing History and Changes

```bash
# Show commit history
git log

# Show commit history (one line per commit)
git log --oneline

# Show commit history with graph
git log --graph --oneline --all

# Show changes in specific file
git log -p filename.txt

# Show differences between working directory and staging
git diff

# Show differences between staging and last commit
git diff --staged

# Show differences between commits
git diff commit1 commit2
```

---

## ↩️ Undoing Changes

```bash
# Discard changes in working directory
git checkout -- filename.txt

# Unstage file (keep changes in working directory)
git reset HEAD filename.txt

# Reset to last commit (lose all changes)
git reset --hard HEAD

# Reset to specific commit (lose changes after that commit)
git reset --hard commit-hash

# Create new commit that undoes previous commit
git revert commit-hash

# Amend last commit message
git commit --amend -m "🐛 Fixed typo in commit message"
```

---

## 🏷️ Tags

```bash
# List all tags
git tag

# Create lightweight tag
git tag v1.0.0

# Create annotated tag
git tag -a v1.0.0 -m "🏷️ Release version 1.0.0"

# Push tags to remote
git push origin --tags

# Delete tag
git tag -d v1.0.0

# Delete tag from remote
git push origin --delete v1.0.0
```

---

## 💡 Best Practices

### 📝 Commit Messages
- Use clear, descriptive commit messages
- Start with an emoji for visual categorization
- Keep the first line under 50 characters
- Use present tense ("Add feature" not "Added feature")

### 🌿 Branching Strategy
- Use `main` branch for production-ready code
- Create feature branches for new features (`feature/user-authentication`)
- Create hotfix branches for urgent fixes (`hotfix/security-patch`)
- Delete branches after merging

### 🔒 Security
- Never commit sensitive information (passwords, API keys, etc.)
- Use `.gitignore` file to exclude sensitive files
- Review changes before committing with `git diff`

### 📁 .gitignore Example
```bash
# Create .gitignore file
touch .gitignore

# Common patterns to ignore
echo "node_modules/" >> .gitignore
echo ".env" >> .gitignore
echo "*.log" >> .gitignore
echo ".DS_Store" >> .gitignore
```

---

## 🆘 Quick Reference

| Command | Description |
|---------|-------------|
| `git init` | Initialize repository |
| `git clone <url>` | Clone repository |
| `git status` | Check status |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Commit changes |
| `git push` | Push to remote |
| `git pull` | Pull from remote |
| `git branch` | List branches |
| `git checkout -b <branch>` | Create and switch branch |
| `git merge <branch>` | Merge branch |

---

## 📚 Additional Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Interactive Git Tutorial](https://learngitbranching.js.org/)

---

**Happy coding!** 🎯 Remember to commit early and commit often!