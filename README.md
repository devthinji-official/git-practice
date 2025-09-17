# Git Commands Cheat Sheet

## 📁 Repository Setup
```bash
git init                          # Initialize new repository
git clone <repo-url>              # Clone existing repository
git clone <repo-url> <directory>  # Clone to specific directory
```

## ⚙️ Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list                 # View all configurations
git config user.name              # Check current username
```

## 📝 Basic Workflow
```bash
# Check status
git status                        # Show working directory status
git diff                          # Show unstaged changes
git diff --staged                 # Show staged changes

# Stage changes
git add <file>                    # Stage specific file
git add .                         # Stage all changes
git add *.js                      # Stage all JS files

# Commit changes
git commit -m "message"           # Commit with message
git commit -am "message"          # Stage and commit all tracked files
git commit --amend                # Modify last commit
```

## 🌿 Branching
```bash
# View branches
git branch                        # List local branches
git branch -r                     # List remote branches
git branch -a                     # List all branches

# Create branches
git branch <branch-name>          # Create new branch
git checkout -b <branch-name>     # Create and switch to branch
git checkout -b <branch> <commit> # Create branch from specific commit

# Switch branches
git checkout <branch-name>        # Switch to branch
git switch <branch-name>          # Modern way to switch branches

# Delete branches
git branch -d <branch-name>       # Delete merged branch
git branch -D <branch-name>       # Force delete branch
git push origin --delete <branch> # Delete remote branch
```

## 🔄 Remote Operations
```bash
# Push changes
git push origin <branch>          # Push to remote branch
git push -u origin <branch>       # Push and set upstream
git push --all                    # Push all branches

# Pull changes
git pull origin <branch>          # Pull from remote branch
git pull                          # Pull from tracked branch
git fetch                         # Download without merging
```

## 🔀 Merging & Integration
```bash
git merge <branch>                # Merge branch into current
git merge --no-ff <branch>        # Merge with merge commit
git rebase <branch>               # Rebase current branch
git rebase -i HEAD~3              # Interactive rebase last 3 commits
```

## 💾 Stashing
```bash
git stash                         # Stash current changes
git stash save "message"          # Stash with message
git stash list                    # List all stashes
git stash pop                     # Apply and remove last stash
git stash apply                   # Apply stash without removing
git stash drop                    # Delete specific stash
```

## ⏪ Undoing Changes
```bash
# Unstage files
git reset HEAD <file>             # Unstage specific file
git reset                         # Unstage all files

# Reset commits
git reset --soft HEAD~1           # Undo commit, keep changes staged
git reset --mixed HEAD~1          # Undo commit, unstage changes
git reset --hard HEAD~1           # Undo commit, delete changes
git reset --hard <commit-hash>    # Reset to specific commit

# Revert commits
git revert <commit-hash>          # Create new commit that undoes changes
```

## 📚 History & Information
```bash
git log                           # View commit history
git log --oneline                 # Compact log view
git log --graph --all             # Visual branch history
git log -p                        # Show patches (changes)
git show <commit-hash>            # Show specific commit details
git blame <file>                  # Show who changed each line
```

## 🏷️ Tags
```bash
git tag                           # List all tags
git tag <tag-name>                # Create lightweight tag
git tag -a <tag-name> -m "msg"    # Create annotated tag
git push origin <tag-name>        # Push specific tag
git push --tags                   # Push all tags
```

---

## 📋 Commit Message Best Practices

### Format Rules
- Use **imperative mood** (commands, not past tense)
- Keep subject line under 50 characters
- Capitalize first letter
- No period at end of subject
- Separate subject and body with blank line

### Good Examples
```
Add user authentication system
Fix memory leak in image processing
Update dependencies to latest versions
Remove deprecated API endpoints
Refactor payment processing module
```

### Think of it as:
> "If applied, this commit will **[your message]**"

### Bad Examples ❌
```
Fixed the bug          # Past tense
added new feature      # Not capitalized
Updated stuff.         # Too vague, has period
WIP                    # Not descriptive
```

### Good Examples ✅
```
Fix login validation bug
Add search functionality to dashboard
Update README with installation steps
Remove unused CSS classes
Refactor user service for better performance
```

---

## 🚨 Common Shortcuts & Tips

| Command | Shortcut | Description |
|---------|----------|-------------|
| `git status` | `git st` | Check status (with alias) |
| `git checkout` | `git co` | Switch branches (with alias) |
| `git branch` | `git br` | List branches (with alias) |
| `git add .` | `git a .` | Stage all files (with alias) |
| `git commit -m` | `git ci -m` | Commit with message (with alias) |

### Set up aliases:
```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
```

---

## 🔥 Emergency Commands
```bash
# Oh no, I committed to wrong branch!
git reset --soft HEAD~1           # Undo commit, keep changes
git stash                         # Stash changes
git checkout <correct-branch>     # Switch to correct branch
git stash pop                     # Apply changes
git add . && git commit           # Commit to correct branch

# I want to undo everything!
git reset --hard HEAD             # Discard all local changes
git clean -fd                     # Remove untracked files/directories
```