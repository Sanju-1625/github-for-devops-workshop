# Git Fetch

## Objective

Learn how to download the latest changes from the remote repository without merging them into the local repository.

---

## Prerequisites

- Git Installed
- Git Configured
- GitHub Repository Created
- Local Repository Available
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

## Step 2: Check Current Status

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

## Step 3: View Current Commit History

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

## Step 4: Fetch Latest Changes

Run

```bash
git fetch origin
```

Expected Output

```text
From https://github.com/username/Git-Practice

* [new branch] feature-login -> origin/feature-login
```

---

## Step 5: Verify Remote Branches

Run

```bash
git branch -r
```

Expected Output

```text
origin/main

origin/feature-login
```

---

## Step 6: Verify Local Branch

Run

```bash
git branch
```

Expected Output

```text
* main
```

---

## Step 7: Compare Local and Remote

Run

```bash
git log --oneline --all --graph
```

Expected Output

```text
Displays local and remote commit history.
```

---

## Step 8: Merge Latest Changes

Run

```bash
git merge origin/main
```

Expected Output

```text
Updating xxxxxx..xxxxxx

Fast-forward
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
git fetch origin
      │
      ▼
Review Changes
      │
      ▼
git merge origin/main
```

---

## Difference Between Git Pull and Git Fetch

| Git Pull | Git Fetch |
|----------|-----------|
| Downloads and merges changes | Downloads changes only |
| Local branch is updated | Local branch is not updated |
| Automatic merge | Manual merge required |

---

## Commands Summary

```bash
git fetch origin

git branch -r

git branch

git log --oneline --all --graph

git merge origin/main
```

---

## Best Practices

- Use `git fetch` before reviewing changes.
- Check incoming commits before merging.
- Use `git fetch` in production environments to avoid unwanted merges.
- Merge only after verifying the changes.

---

## Common Mistakes

### Mistake 1

Assuming `git fetch` updates the local branch.

Error

```text
Local files do not change.
```

Solution

```bash
git merge origin/main
```

---

### Mistake 2

Forgetting to merge after fetch.

Solution

```bash
git fetch origin

git merge origin/main
```

---

### Mistake 3

Confusing `git fetch` with `git pull`.

Remember

```text
git fetch = Download only

git pull = Download + Merge
```

---

## Interview Questions

1. What is Git Fetch?

2. Why do we use `git fetch`?

3. What is the difference between `git fetch` and `git pull`?

4. Does `git fetch` modify the local branch?

5. Which command downloads changes without merging them?

6. When should you use `git fetch`?

7. What should you do after `git fetch` if you want the latest code?
