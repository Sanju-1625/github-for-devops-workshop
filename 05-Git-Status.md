# Git Status

## Objective

Learn how to check the current status of a Git repository.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created

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

No commits yet

nothing to commit
```

---

## Step 3: Create a New File

Run

```bash
touch index.html
```

Verify

```bash
ls
```

Expected Output

```text
README.md
index.html
```

---

## Step 4: Check Status Again

Run

```bash
git status
```

Expected Output

```text
On branch main

No commits yet

Untracked files:

index.html

nothing added to commit but untracked files present
```

---

## Step 5: Stage the File

Run

```bash
git add index.html
```

---

## Step 6: Check Status Again

Run

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: index.html
```

---

## Step 7: Modify the File

Run

```bash
echo "Hello Git" >> index.html
```

---

## Step 8: Check Status

Run

```bash
git status
```

Expected Output

```text
Changes not staged for commit
```

---

## File Status Flow

```text
Create File
      │
      ▼
Untracked
      │
git add
      │
      ▼
Staged
      │
git commit
      │
      ▼
Tracked
      │
Modify File
      │
      ▼
Modified
```

---

## Commands Summary

```bash
git status

touch index.html

git add index.html

echo "Hello Git" >> index.html
```

---

## Interview Questions

1. What is the purpose of the `git status` command?

2. What is an untracked file?

3. What is a staged file?

4. What is a tracked file?

5. How do you check the current status of a Git repository?

6. When should you use `git status`?

7. Can `git status` modify any files?
