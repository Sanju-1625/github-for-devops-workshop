# Git Interview Questions

## Objective

Practice Git interview questions from Beginner to 3 Years DevOps Engineer level.

---

# Beginner Level

## Question 1

What is Git?

### Answer

Git is a Distributed Version Control System (DVCS) used to track changes in source code and collaborate with multiple developers.

---

## Question 2

Why do we use Git?

### Answer

- Track code changes
- Maintain version history
- Collaborate with developers
- Rollback to previous versions
- Manage source code

---

## Question 3

What is Version Control?

### Answer

Version Control is a system that records changes made to files over time and allows us to restore previous versions whenever required.

---

## Question 4

What is a Repository?

### Answer

A Repository is a storage location where Git manages project files and tracks all changes.

---

## Question 5

Difference between Git and GitHub?

### Answer

| Git | GitHub |
|------|---------|
| Version Control System | Cloud Hosting Platform |
| Installed on Local Machine | Stores Git Repositories Online |
| Tracks Changes | Team Collaboration |

---

# Intermediate Level

## Question 6

What does git status do?

### Answer

Shows

- Current Branch
- Modified Files
- Staged Files
- Untracked Files
- Repository Status

---

## Question 7

What is git add?

### Answer

Moves files from the Working Directory to the Staging Area.

---

## Question 8

What is git commit?

### Answer

Saves staged changes permanently in the local Git repository.

---

## Question 9

What is git log?

### Answer

Displays commit history.

---

## Question 10

Difference between git fetch and git pull?

### Answer

| Git Fetch | Git Pull |
|------------|-----------|
| Downloads changes only | Downloads and merges changes |
| No merge | Automatic merge |

---

## Question 11

What is a Branch?

### Answer

A Branch is an independent line of development used to work on a feature without affecting the main branch.

---

## Question 12

Why do companies use Branches?

### Answer

- Feature Development
- Bug Fixes
- Team Collaboration
- Safe Development

---

## Question 13

What is Git Merge?

### Answer

Combines changes from one branch into another branch.

---

## Question 14

What is a Merge Conflict?

### Answer

A Merge Conflict occurs when Git cannot automatically merge changes because the same file or line was modified in different branches.

---

## Question 15

How do you resolve a Merge Conflict?

### Answer

```text
Open conflicted file
        │
        ▼
Resolve conflict
        │
        ▼
git add .
        │
        ▼
git commit
```

---

## Question 16

What is Git Rebase?

### Answer

Git Rebase moves commits from one branch to another and creates a clean commit history.

---

## Question 17

Difference between Merge and Rebase?

### Answer

| Merge | Rebase |
|--------|---------|
| Creates Merge Commit | No Merge Commit |
| Complete History | Clean History |

---

## Question 18

What is Git Stash?

### Answer

Temporarily saves uncommitted changes without creating a commit.

---

## Question 19

What is Git Tag?

### Answer

A Git Tag marks important project versions like releases.

Example

```text
v1.0

v2.0
```

---

## Question 20

What is a Pull Request?

### Answer

A Pull Request is used to request code review before merging changes into the main branch.

---

# Real-Time DevOps Level

## Question 21

Explain the Git workflow followed in your company.

### Answer

```text
Clone Repository
        │
        ▼
Create Feature Branch
        │
        ▼
Develop Code
        │
        ▼
git status
        │
        ▼
git add .
        │
        ▼
git commit
        │
        ▼
git push
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
Merge
        │
        ▼
CI/CD Pipeline
        │
        ▼
Deployment
```

---

## Question 22

Why shouldn't developers work directly on the main branch?

### Answer

Because it may introduce bugs into production. Developers should work in feature branches and merge changes only after code review.

---

## Question 23

When do you use git stash?

### Answer

When I have unfinished work and need to switch to another branch or fix an urgent issue.

---

## Question 24

How do you verify the current branch?

### Answer

```bash
git branch
```

---

## Question 25

How do you see commit history?

### Answer

```bash
git log

git log --oneline
```

---

## Question 26

How do you undo an uncommitted change?

### Answer

```bash
git restore <file-name>
```

---

## Question 27

How do you delete a local branch?

### Answer

```bash
git branch -d branch-name
```

---

## Question 28

How do you delete a remote branch?

### Answer

```bash
git push origin --delete branch-name
```

---

## Question 29

What do you do if git push is rejected?

### Answer

```text
1. Pull latest changes.

2. Resolve conflicts if any.

3. Commit changes.

4. Push again.
```

---

## Question 30

Which Git commands do you use daily?

### Answer

```bash
git status

git pull

git branch

git switch

git add .

git commit -m "message"

git push

git log

git stash
```

---

# Most Frequently Asked Commands

```bash
git status

git add .

git commit -m "message"

git push

git pull

git fetch

git branch

git switch

git merge

git rebase

git stash

git tag

git log

git clone
```

---

# Quick Revision

```text
Repository
      │
      ▼
Branch
      │
      ▼
Code Changes
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
git push
      │
      ▼
Pull Request
      │
      ▼
Code Review
      │
      ▼
Merge
      │
      ▼
Deployment
```

---

# Interview Tips

- Answer with real-time examples.
- Explain the workflow instead of only commands.
- Mention best practices.
- Describe how Git is used in team collaboration.
- Keep answers simple and structured.
