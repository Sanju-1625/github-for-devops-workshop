# Git Pull

## Objective

Learn how to download the latest changes from the remote GitHub repository to your local repository.

---

## Prerequisites

- Git Installed
- Git Configured
- GitHub Repository Created
- Local Repository Cloned
- Remote Repository Available

---

## Step 1: Open Git Repository

Run

```bash
cd Git-Practice
```

Verify

```bash
pwd
```

Expected Output

```text
Current directory should be Git-Practice
```

---

## Step 2: Check Repository Status

Run

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Step 3: Verify Remote Repository

Run

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/Git-Practice.git (fetch)

origin  https://github.com/username/Git-Practice.git (push)
```

---

## Step 4: Pull Latest Changes

Run

```bash
git pull origin main
```

Expected Output

```text
From https://github.com/username/Git-Practice

* branch            main -> FETCH_HEAD

Updating xxxxxx..xxxxxx

Fast-forward
```

---

## Step 5: Verify Latest Files

Run

```bash
ls
```

Expected Output

```text
README.md

index.html

style.css

about.html
```

---

## Step 6: Verify Commit History

Run

```bash
git log --oneline
```

Expected Output

```text
a12bc34 Updated README

b45de67 Added about page

c78fg90 Initial commit
```

---

## Step 7: Verify Repository Status

Run

```bash
git status
```

Expected Output

```text
On branch main

Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

## Real-Time Workflow

```text
Developer 1
      │
      ▼
git push origin main
      │
      ▼
GitHub Repository Updated
      │
      ▼
Developer 2
      │
      ▼
git pull origin main
      │
      ▼
Latest Code Downloaded
```

---

## Commands Summary

```bash
git pull origin main

git status

git log --oneline

git remote -v

ls
```

---

## Best Practices

- Pull the latest code before starting work.
- Pull before pushing your changes.
- Resolve merge conflicts if they occur.
- Check `git status` after pulling.

---

## Common Mistakes

### Mistake 1

Pulling from the wrong branch.

Error

```text
Already up to date.
```

Solution

```bash
git branch

git pull origin main
```

---

### Mistake 2

Merge Conflict During Pull.

Error

```text
Automatic merge failed.
```

Solution

Resolve the conflict.

```bash
git add .

git commit -m "Resolved merge conflict"
```

---

### Mistake 3

No Remote Repository

Error

```text
fatal: 'origin' does not appear to be a git repository
```

Solution

```bash
git remote add origin <repository-url>
```

---

## Interview Questions

1. What is Git Pull?

2. Why do we use `git pull`?

3. Which command downloads the latest changes from GitHub?

4. What is the difference between `git pull` and `git push`?

5. When should a developer use `git pull`?

6. What happens if two developers modify the same file?

7. What should you do before pushing your code?
