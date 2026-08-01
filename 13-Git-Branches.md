# Git Branches

## Objective

Learn how to create, switch, rename, list and delete Git branches.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one commit available

---

## Step 1: Check Current Branch

Run

```bash
git branch
```

Expected Output

```text
* main
```

---

## Step 2: Create a New Branch

Run

```bash
git branch feature-login
```

Verify

```bash
git branch
```

Expected Output

```text
feature-login
* main
```

---

## Step 3: Switch to New Branch

Run

```bash
git switch feature-login
```

Verify

```bash
git branch
```

Expected Output

```text
* feature-login
main
```

---

## Step 4: Create a New File

Run

```bash
touch login.html
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
login.html
```

---

## Step 5: Check Status

Run

```bash
git status
```

Expected Output

```text
Untracked files:

login.html
```

---

## Step 6: Stage the File

Run

```bash
git add .
```

Verify

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: login.html
```

---

## Step 7: Commit the Changes

Run

```bash
git commit -m "Added login page"
```

Expected Output

```text
[feature-login xxxxxx] Added login page
```

---

## Step 8: Switch Back to Main Branch

Run

```bash
git switch main
```

Verify

```bash
ls
```

Expected Output

```text
login.html is not available.
```

---

## Step 9: Merge Branch (Preview)

Run

```bash
git merge feature-login
```

Expected Output

```text
Updating xxxxxx..xxxxxx

Fast-forward
```

---

## Step 10: Verify Merge

Run

```bash
ls
```

Expected Output

```text
README.md
index.html
style.css
login.html
```

---

## Step 11: Create Another Branch

Run

```bash
git branch feature-payment
```

Verify

```bash
git branch
```

Expected Output

```text
feature-payment
feature-login
* main
```

---

## Step 12: Rename Branch

Run

```bash
git branch -m feature-payment payment-feature
```

Verify

```bash
git branch
```

Expected Output

```text
payment-feature
feature-login
* main
```

---

## Step 13: Delete Branch

Run

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Step 14: Force Delete Branch

Run

```bash
git branch -D payment-feature
```

Expected Output

```text
Deleted branch payment-feature
```

---

## Real-Time Workflow

```text
Create Branch
      │
      ▼
Develop Feature
      │
      ▼
git add .
      │
      ▼
git commit
      │
      ▼
Switch to Main
      │
      ▼
Merge Branch
      │
      ▼
Delete Branch
```

---

## Commands Summary

```bash
git branch

git branch feature-login

git switch feature-login

git switch main

git branch -m old-name new-name

git branch -d feature-login

git branch -D feature-login
```

---

## Best Practices

- Create one branch for one feature.
- Use meaningful branch names.
- Commit changes before switching branches.
- Delete merged branches.
- Never develop directly on the main branch.

---

## Common Mistakes

### Mistake 1

Trying to delete the current branch.

Error

```text
Cannot delete branch currently checked out.
```

Solution

```bash
git switch main

git branch -d feature-login
```

---

### Mistake 2

Deleting a branch without merging.

Error

```text
The branch is not fully merged.
```

Solution

Merge the branch first or use:

```bash
git branch -D feature-login
```

---

### Mistake 3

Working on the wrong branch.

Solution

Always verify before starting work.

```bash
git branch
```

---

## Real-Time Interview Scenario

**Question**

Three developers are working on Login, Payment and Dashboard features.

Should all developers work on the **main** branch?

**Answer**

No.

Each developer should create a separate feature branch.

After development and testing, the feature branch should be merged into the main branch.

---

## Interview Questions

1. What is a Git Branch?

2. Why do we use branches?

3. How do you create a branch?

4. How do you switch between branches?

5. How do you rename a branch?

6. How do you delete a branch?

7. Why should developers avoid working directly on the main branch?

8. What happens when you switch branches?

9. What is a feature branch?

10. Which command lists all local branches?
