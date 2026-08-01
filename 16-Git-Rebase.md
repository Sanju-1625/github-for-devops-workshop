# Git Rebase

## Objective

Learn how to move commits from one branch to another and maintain a clean commit history.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least two branches available
- Commits available in both branches

---

## Step 1: Check Current Branch

Run

```bash
git branch
```

Expected Output

```text
* feature-login
main
```

---

## Step 2: View Commit History

Run

```bash
git log --oneline
```

Expected Output

```text
a123456 Added Login Page

b234567 Updated README

c345678 Initial Commit
```

---

## Step 3: Switch to Feature Branch

Run

```bash
git switch feature-login
```

Expected Output

```text
Switched to branch 'feature-login'
```

---

## Step 4: Rebase Feature Branch

Run

```bash
git rebase main
```

Expected Output

```text
Successfully rebased and updated refs/heads/feature-login.
```

---

## Step 5: Verify Commit History

Run

```bash
git log --oneline --graph
```

Expected Output

```text
* a123456 Added Login Page

* b234567 Updated README

* c345678 Initial Commit
```

---

## Step 6: Switch to Main Branch

Run

```bash
git switch main
```

---

## Step 7: Merge Rebased Branch

Run

```bash
git merge feature-login
```

Expected Output

```text
Fast-forward
```

---

## Real-Time Workflow

```text
main
    │
    ▼
Latest Commits
    │
    ▼
feature-login
    │
    ▼
git rebase main
    │
    ▼
Updated Commit History
    │
    ▼
git merge feature-login
```

---

## Difference Between Merge and Rebase

| Git Merge | Git Rebase |
|------------|------------|
| Creates a Merge Commit | No Merge Commit |
| Keeps Complete History | Creates Clean History |
| Easy to Understand | Cleaner Commit History |
| Used Frequently | Used Before Merge |

---

## Commands Summary

```bash
git switch feature-login

git rebase main

git switch main

git merge feature-login

git log --oneline --graph
```

---

## Best Practices

- Rebase only your own feature branch.
- Pull the latest changes before rebasing.
- Verify commit history after rebase.
- Use rebase to keep commit history clean.

---

## Common Mistakes

### Mistake 1

Rebasing the main branch.

Solution

```bash
git switch feature-login

git rebase main
```

---

### Mistake 2

Rebasing shared branches.

Solution

Avoid rebasing branches that other developers are using.

---

### Mistake 3

Ignoring Rebase Conflicts.

Solution

Resolve the conflict.

Run

```bash
git add .
```

Continue Rebase

```bash
git rebase --continue
```

---

## Real-Time Interview Scenario

**Question**

The main branch has new commits.

Your feature branch is behind.

What should you do before creating a Pull Request?

**Answer**

```text
Switch to feature branch
        │
        ▼
git rebase main
        │
        ▼
Resolve conflicts (if any)
        │
        ▼
git rebase --continue
        │
        ▼
Push the updated branch
```

---

## Interview Questions

1. What is Git Rebase?

2. Why do we use Git Rebase?

3. What is the difference between Merge and Rebase?

4. Which command is used to rebase a branch?

5. Can Rebase create merge conflicts?

6. What should you do after resolving a rebase conflict?

7. When should you avoid using Git Rebase?

8. Why do companies use Git Rebase?

9. What is the purpose of `git rebase --continue`?

10. Which is better: Merge or Rebase?
