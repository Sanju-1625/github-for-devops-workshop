# Git Commit

## Objective

Learn how to save staged changes permanently in the Git repository.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- Files Added to Staging Area

---

## Step 1: Check Repository Status

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

## Step 2: Commit the Changes

Run

```bash
git commit -m "Initial commit"
```

Expected Output

```text
[main (root-commit) xxxxxx] Initial commit
2 files changed
create mode 100644 index.html
create mode 100644 style.css
```

---

## Step 3: Verify Commit

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

## Step 4: Modify a File

Run

```bash
echo "Welcome to Git" >> index.html
```

---

## Step 5: Check Status

Run

```bash
git status
```

Expected Output

```text
Changes not staged for commit
```

---

## Step 6: Stage the Changes

Run

```bash
git add index.html
```

---

## Step 7: Commit Again

Run

```bash
git commit -m "Updated index.html"
```

Expected Output

```text
[main xxxxxx] Updated index.html
1 file changed
```

---

## Step 8: Verify

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

## Commit Workflow

```text
Create File
      │
      ▼
git status
      │
      ▼
git add
      │
      ▼
git commit
      │
      ▼
Changes Saved
```

---

## Commit Message Examples

```bash
git commit -m "Initial commit"

git commit -m "Added login page"

git commit -m "Fixed login bug"

git commit -m "Updated README"

git commit -m "Added CSS styles"
```

---

## Commands Summary

```bash
git commit -m "Initial commit"

git commit -m "Added login page"

git commit -m "Updated README"

git status

git add .
```

---

## Best Practices

- Write meaningful commit messages.
- Keep one commit for one logical change.
- Commit frequently.
- Always check `git status` before committing.

---

## Common Mistakes

### Mistake 1

Trying to commit without staging files.

```bash
git commit -m "First commit"
```

Error

```text
nothing added to commit
```

Solution

```bash
git add .
git commit -m "First commit"
```

---

### Mistake 2

Writing unclear commit messages.

❌ Bad

```text
update
```

✅ Good

```text
Added login feature
```

---

## Interview Questions

1. What is Git Commit?

2. Why do we use Git Commit?

3. What is the purpose of the `-m` option?

4. Can you commit without using `git add`?

5. What happens after a successful commit?

6. What is a good commit message?

7. Which command saves changes permanently in the local repository?
