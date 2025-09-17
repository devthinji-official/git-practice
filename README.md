# Git Commands

```bash
# Initialize or clone a repository
git init
git clone <repo>

# Stage and commit changes
git add <file>
git commit -m "message"

# Push and pull
git push origin <branch>
git pull origin <branch>

# Branching
git branch <branch>
git checkout <branch>
git checkout -b <branch>       # Create and switch to a new branch

# Delete branch
git branch -d <branch>

# Branching from a specific commit
git checkout -b <branch> <commit-hash>

# Branching from another branch
git branch <new-branch> <source-branch>

# Publish a new branch
git push --set-upstream origin <branch>

--set-upstream can be shortened to -u
--set-upstream is useful when pushing a branch for the first time and linking local branch to remote branch

# Reset to a specific commit
git reset --hard <commit-hash>

# Merging and related
git merge <branch>
git rebase <branch>
git stash

# History
git log
```

---

# Git Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

---

# Commit Messages

* Must be **meaningful** and written in the **imperative mood** (like commands).
* Examples:

  * `Fix bug in user login`
  * `Add search functionality`
  * `Update README with setup instructions`

👉 Think of commit messages as answers to:

* *“If applied to the codebase, this commit will…”*
* *“What will happen when I merge the branch containing this commit?”*

So you’re essentially writing: **“It will…”**
