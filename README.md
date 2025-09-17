# GIT COMMANDS

```bash
git init
git clone <repo>
git add <file>
git commit -m "message"

git push origin <branch>
git pull origin <branch>

# Branching
git branch <branch>
git checkout <branch>

# Merging
git merge <branch>
git rebase <branch>
git stash
git log
```

# git identity

```bash
git config --global user.name "Your Name"
git config --global user.email "
git config --list
```

# Create branch and switch to it

```bash
git checkout -b <branch>
```

# Delete branch

```bash
git branch -d <branch>
```

# branching from a specific commit

```bash
git checkout -b <branch> <commit-hash>
```
# Reset to a specific commit

```bash
git reset --hard <commit-hash>
```

# branch from a specific branch

```bash
git branch <new-branch> <source-branch>

```


# Commit messages has to be meaningful and imperative
# Example: "Fix bug in user login", like giving commands


It is like they are answering the question:-

`If applied to the codebase, this commit will...`
...Or...
`What will happen, when I merge the branch containing this commit?`

Think....`It will....`