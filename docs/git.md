# Git

## basic usage

### init a repo

```bash
git init
```

### Staging files

```bash
git add .
```

### commiting changes

```bash
git commit -m "your comment"
```

## branches

note that you need to write the precise branch name to
preform action on it

### listing branches

```bash
git branch
```

### create a new branch

```bash
git branch new-branch-name
```

there is also another way to create a branch
which is a kind of shortcut that will create and switch to the newly created branch

```bash
git checkout -b new-branch-name
```

### changing current branch

```bash
git checkout branch-name
```

### deleting branch name

```bash
git branch -d branch-name-to-delete
```
