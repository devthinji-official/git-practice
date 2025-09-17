# This is a test README file and a test project.

The safe alternative is:

```sh
git switch main
```

✅ If you have uncommitted changes, Git will stop and warn you instead of discarding them.

👉 If you *do* want to keep changes when switching, you can stash first:

```sh
git stash
git switch main
git stash pop
```

When you’d actually need the **force**

```sh
git switch -f main
```