# Git Stash

## Objective

Learn how to temporarily save uncommitted changes without creating a commit.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one modified file

---

## Step 1: Check Repository Status

Run

```bash
git status
```

Expected Output

```text
Changes not staged for commit:

modified: README.md
```

---

## Step 2: Save Changes to Stash

Run

```bash
git stash
```

Expected Output

```text
Saved working directory and index state WIP on main.
```

---

## Step 3: Verify Working Directory

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

## Step 4: View Stash List

Run

```bash
git stash list
```

Expected Output

```text
stash@{0}: WIP on main
```

---

## Step 5: Continue Other Work

Example

```bash
git switch feature-login
```

Do your work.

Commit if required.

---

## Step 6: Switch Back

Run

```bash
git switch main
```

---

## Step 7: Apply Stashed Changes

Run

```bash
git stash apply
```

Expected Output

```text
Changes are restored.

README.md modified.
```

---

## Step 8: Verify

Run

```bash
git status
```

Expected Output

```text
modified: README.md
```

---

## Step 9: Remove Stash

Run

```bash
git stash drop
```

Expected Output

```text
Dropped stash@{0}
```

---

## Step 10: Verify Stash List

Run

```bash
git stash list
```

Expected Output

```text
No stash entries found.
```

---

## Step 11: Apply and Delete Stash Together

Run

```bash
git stash pop
```

Expected Output

```text
Applied stash.

Dropped stash@{0}
```

---

## Real-Time Workflow

```text
Working on Feature A
        │
        ▼
Urgent Bug Assigned
        │
        ▼
git stash
        │
        ▼
Switch Branch
        │
        ▼
Fix Bug
        │
        ▼
Commit Changes
        │
        ▼
Switch Back
        │
        ▼
git stash pop
        │
        ▼
Continue Previous Work
```

---

## Commands Summary

```bash
git stash

git stash list

git stash apply

git stash pop

git stash drop

git status
```

---

## Best Practices

- Use stash only for temporary changes.
- Commit completed work instead of stashing.
- Check the stash list regularly.
- Remove unused stashes.

---

## Common Mistakes

### Mistake 1

Forgetting stashed changes.

Solution

```bash
git stash list
```

---

### Mistake 2

Applying the wrong stash.

Solution

```bash
git stash list

git stash apply stash@{0}
```

---

### Mistake 3

Using `git stash apply` repeatedly.

Solution

Use

```bash
git stash pop
```

when you no longer need the stash.

---

## Real-Time Interview Scenario

**Question**

You are working on a feature.

Your manager asks you to fix a production issue immediately.

Your current changes are incomplete.

What will you do?

**Answer**

```text
Save current work
        │
        ▼
git stash
        │
        ▼
Switch Branch
        │
        ▼
Fix Production Issue
        │
        ▼
Commit & Push
        │
        ▼
Switch Back
        │
        ▼
git stash pop
        │
        ▼
Continue Previous Work
```

---

## Interview Questions

1. What is Git Stash?

2. Why do we use Git Stash?

3. What is the difference between `git stash apply` and `git stash pop`?

4. Which command shows all stashes?

5. Which command removes a stash?

6. Can Git Stash save uncommitted changes?

7. When do you use Git Stash in real projects?

8. Can you have multiple stashes?

9. Which command applies a specific stash?

10. What happens after running `git stash pop`?
