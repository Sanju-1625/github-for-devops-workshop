# GitHub Pull Request (PR)

## Objective

Learn how to create, review, approve, and merge a Pull Request in GitHub.

---

## Prerequisites

- Git Installed
- Git Configured
- GitHub Account
- GitHub Repository Created
- Feature Branch Created
- Changes Committed and Pushed

---

## Step 1: Create a Feature Branch

Run

```bash
git switch -c feature-login
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

## Step 2: Make Changes

Example

```bash
touch login.html
```

---

## Step 3: Stage Changes

Run

```bash
git add .
```

---

## Step 4: Commit Changes

Run

```bash
git commit -m "Added login page"
```

Expected Output

```text
[feature-login xxxxxx] Added login page
```

---

## Step 5: Push Feature Branch

Run

```bash
git push origin feature-login
```

Expected Output

```text
Branch 'feature-login' set up to track remote branch.
```

---

## Step 6: Open GitHub

Open your GitHub repository.

You will see:

```text
Compare & pull request
```

Click it.

---

## Step 7: Create Pull Request

Verify

```text
Base Branch : main

Compare Branch : feature-login
```

Add

Title

```text
Added Login Feature
```

Description

```text
Implemented Login Page

Added HTML file

Ready for review
```

Click

```text
Create Pull Request
```

---

## Step 8: Code Review

Reviewer checks

- Code Quality
- Best Practices
- Bugs
- Security Issues
- Coding Standards

If changes are required

```text
Reviewer requests changes.
```

Developer updates the code.

Push again

```bash
git add .

git commit -m "Addressed review comments"

git push origin feature-login
```

The Pull Request is updated automatically.

---

## Step 9: Merge Pull Request

Click

```text
Merge Pull Request
```

Then

```text
Confirm Merge
```

Expected Output

```text
Pull Request successfully merged.
```

---

## Step 10: Delete Feature Branch

GitHub shows

```text
Delete Branch
```

Click it.

Or use Git

```bash
git branch -d feature-login

git push origin --delete feature-login
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
git push origin feature-login
        │
        ▼
Create Pull Request
        │
        ▼
Code Review
        │
        ▼
Approve
        │
        ▼
Merge PR
        │
        ▼
Delete Feature Branch
```

---

## Commands Summary

```bash
git switch -c feature-login

git add .

git commit -m "Added login page"

git push origin feature-login

git branch -d feature-login

git push origin --delete feature-login
```

---

## Best Practices

- Create one Pull Request for one feature.
- Write a meaningful PR title.
- Add a clear description.
- Resolve review comments.
- Merge only after approval.
- Delete the feature branch after merging.

---

## Common Mistakes

### Mistake 1

Creating a Pull Request directly to the wrong branch.

Solution

Verify

```text
Base Branch = main
```

---

### Mistake 2

Merging without code review.

Solution

Always wait for reviewer approval.

---

### Mistake 3

Forgetting to delete the feature branch.

Solution

Delete it after merging.

---

## Real-Time Interview Scenario

**Question**

A developer completed the Login feature.

What is the correct workflow before the code reaches the main branch?

**Answer**

```text
Create Feature Branch
        │
        ▼
Develop Feature
        │
        ▼
Commit Changes
        │
        ▼
Push Feature Branch
        │
        ▼
Create Pull Request
        │
        ▼
Reviewer Reviews Code
        │
        ▼
Approve Pull Request
        │
        ▼
Merge into Main Branch
        │
        ▼
Delete Feature Branch
```

---

## Interview Questions

1. What is a Pull Request?

2. Why do companies use Pull Requests?

3. Who reviews a Pull Request?

4. Can a Pull Request be updated after creation?

5. What happens after a Pull Request is approved?

6. Why should we not push directly to the main branch?

7. What information should be included in a Pull Request?

8. What is the difference between Git Merge and GitHub Pull Request?

9. What is code review?

10. What is the complete Pull Request workflow in GitHub?
