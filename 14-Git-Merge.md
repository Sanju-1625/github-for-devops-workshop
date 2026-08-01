# Git Merge

## Objective

Learn how to merge changes from one branch into another branch.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one feature branch available
- At least one commit in both branches

---

## Step 1: Check Current Branch

Run

```bash
git branch
```

Expected Output

```text
feature-login
* main
```

---

## Step 2: Switch to Main Branch

Run

```bash
git switch main
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

## Step 3: Merge Feature Branch

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

## Step 4: Verify Merge

Run

```bash
git log --oneline
```

Expected Output

```text
a12bc34 Added login feature

b45de67 Initial commit
```

---

## Step 5: Verify Files

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

## Step 6: Check Repository Status

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

## Step 7: Delete Merged Branch

Run

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Real-Time Workflow

```text
Create Feature Branch
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
git merge feature-login
        │
        ▼
Delete Feature Branch
```

---

## Commands Summary

```bash
git switch main

git merge feature-login

git log --oneline

git status

git branch -d feature-login
```

---

## Best Practices

- Merge only tested code.
- Switch to the target branch before merging.
- Delete feature branches after a successful merge.
- Always check `git status` before merging.
- Pull the latest changes before merging in a team environment.

---

## Common Mistakes

### Mistake 1

Trying to merge from the wrong branch.

Error

```text
Code merged into the wrong branch.
```

Solution

```bash
git branch

git switch main

git merge feature-login
```

---

### Mistake 2

Trying to merge a branch that does not exist.

Error

```text
merge: feature-login - not something we can merge
```

Solution

```bash
git branch
```

Verify the branch name and merge again.

---

### Mistake 3

Deleting a branch before merging.

Solution

Always merge first.

```bash
git merge feature-login

git branch -d feature-login
```

---

## Real-Time Interview Scenario

**Question**

A developer completed the Login feature in the `feature-login` branch.

Testing is successful.

What should be the next step?

**Answer**

```text
Switch to main branch
        │
        ▼
Merge feature-login
        │
        ▼
Verify code
        │
        ▼
Delete feature-login branch
```

---

## Interview Questions

1. What is Git Merge?

2. Why do we use Git Merge?

3. Which command is used to merge a branch?

4. Which branch should you switch to before merging?

5. What happens after a successful merge?

6. Can you merge a branch without switching to the target branch?

7. Why should merged branches be deleted?

8. What is a Fast-Forward Merge?

9. What should you verify after merging?

10. What is the difference between creating a branch and merging a branch?
