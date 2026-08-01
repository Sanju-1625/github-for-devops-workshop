# Git Add

## Objective

Learn how to stage files before creating a commit.

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
Untracked files:

index.html
```

---

## Step 3: Add a Single File

Run

```bash
git add index.html
```

---

## Step 4: Verify

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

## Step 5: Create Another File

Run

```bash
touch style.css
```

Verify

```bash
ls
```

Expected Output

```text
README.md
index.html
style.css
```

---

## Step 6: Check Status

Run

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: index.html

Untracked files:

style.css
```

---

## Step 7: Add Multiple Files

Run

```bash
git add .
```

---

## Step 8: Verify

Run

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: index.html

new file: style.css
```

---

## Step 9: Modify a File

Run

```bash
echo "Git Learning" >> index.html
```

---

## Step 10: Check Status

Run

```bash
git status
```

Expected Output

```text
Changes not staged for commit
```

---

## Step 11: Stage Modified File

Run

```bash
git add index.html
```

---

## Step 12: Verify

Run

```bash
git status
```

Expected Output

```text
Changes to be committed
```

---

## Commands Summary

```bash
git add index.html

git add style.css

git add .

git status
```

---

## Important Notes

```text
git add file_name    -> Stage one file

git add .            -> Stage all files in the current directory

git add -A           -> Stage all changes in the repository
```

---

## Interview Questions

1. What is the purpose of the `git add` command?

2. What is the difference between `git add file_name` and `git add .`?

3. What happens after running `git add`?

4. Can we commit a file without using `git add`?

5. How do you stage all files in a repository?

6. What is a staged file?
