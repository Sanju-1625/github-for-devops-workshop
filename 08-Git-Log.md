# Git Log

## Objective

Learn how to view the commit history of a Git repository.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one commit available

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

## Step 2: View Commit History

Run

```bash
git log
```

Expected Output

```text
commit 7f9d2d9a4f6d8c...

Author: Sanju Kumar <sanju@example.com>

Date: Mon Aug 04 10:30:45 2026

    Initial commit
```

---

## Step 3: Add a New File

Run

```bash
touch about.html
```

---

## Step 4: Stage the File

Run

```bash
git add about.html
```

---

## Step 5: Commit the File

Run

```bash
git commit -m "Added about page"
```

Expected Output

```text
[main xxxxxx] Added about page
1 file changed
```

---

## Step 6: View Commit History Again

Run

```bash
git log
```

Expected Output

```text
commit xxxxxxxxx

Author: Sanju Kumar

Date: ...

    Added about page

commit xxxxxxxxx

Author: Sanju Kumar

Date: ...

    Initial commit
```

---

## Step 7: View Short Commit History

Run

```bash
git log --oneline
```

Expected Output

```text
a12bc34 Added about page

d45ef67 Initial commit
```

---

## Step 8: View Last 2 Commits

Run

```bash
git log -2
```

Expected Output

```text
Shows only the last two commits.
```

---

## Step 9: View Commit History with Graph

Run

```bash
git log --oneline --graph
```

Expected Output

```text
* a12bc34 Added about page

* d45ef67 Initial commit
```

---

## Commands Summary

```bash
git log

git log --oneline

git log -2

git log --oneline --graph
```

---

## Best Practices

- Check commit history before reverting changes.
- Write meaningful commit messages.
- Use `git log --oneline` for quick review.
- Review commit history before merging branches.

---

## Common Mistakes

### Mistake 1

Running `git log` in a folder that is not a Git repository.

Error

```text
fatal: not a git repository
```

Solution

```bash
cd Git-Practice
```

---

### Mistake 2

No commits available.

Error

```text
fatal: your current branch does not have any commits yet
```

Solution

```bash
git add .
git commit -m "Initial commit"
```

---

## Interview Questions

1. What is Git Log?

2. Why do we use `git log`?

3. Which command shows commit history?

4. Which command displays commit history in one line?

5. Which command shows only the last 2 commits?

6. Why is commit history important?

7. What information does `git log` display?
