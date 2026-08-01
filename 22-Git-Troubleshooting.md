# Git Troubleshooting

## Objective

Learn how to identify and resolve common Git issues in real-world projects.

---

## Scenario 1: Git Not Installed

Error

```text
git : The term 'git' is not recognized
```

Solution

```text
1. Download Git

https://git-scm.com/downloads

2. Install Git

3. Restart Terminal

4. Verify

git --version
```

---

## Scenario 2: Repository Not Initialized

Error

```text
fatal: not a git repository
```

Solution

```bash
git init
```

Verify

```bash
git status
```

---

## Scenario 3: Git Username Not Configured

Error

```text
Author identity unknown
```

Solution

```bash
git config --global user.name "Your Name"

git config --global user.email "your@email.com"
```

Verify

```bash
git config --list
```

---

## Scenario 4: Nothing to Commit

Error

```text
nothing to commit, working tree clean
```

Reason

```text
No changes available.
```

Solution

Modify a file.

Check

```bash
git status
```

---

## Scenario 5: Forgot git add

Error

```text
no changes added to commit
```

Solution

```bash
git add .

git commit -m "message"
```

---

## Scenario 6: Push Rejected

Error

```text
Updates were rejected because the remote contains work that you do not have locally.
```

Solution

```bash
git pull origin main

git push origin main
```

---

## Scenario 7: Merge Conflict

Error

```text
CONFLICT (content)
```

Solution

```text
Open File

Resolve Conflict

Remove Conflict Markers

Save File
```

Run

```bash
git add .

git commit -m "Resolved Merge Conflict"
```

---

## Scenario 8: Wrong Branch

Problem

```text
Code committed in wrong branch.
```

Solution

Check

```bash
git branch
```

Switch

```bash
git switch branch-name
```

---

## Scenario 9: Branch Already Exists

Error

```text
fatal: A branch named 'feature-login' already exists.
```

Solution

View Branches

```bash
git branch
```

Switch

```bash
git switch feature-login
```

---

## Scenario 10: Repository Already Exists

Error

```text
destination path already exists
```

Solution

Choose another folder.

OR

Delete the existing folder.

Clone again.

---

## Scenario 11: Authentication Failed

Error

```text
Authentication failed
```

Solution

- Verify GitHub username.
- Use Personal Access Token (PAT).
- Configure SSH if required.

---

## Scenario 12: Remote Already Exists

Error

```text
remote origin already exists
```

Solution

Check

```bash
git remote -v
```

Remove

```bash
git remote remove origin
```

Add Again

```bash
git remote add origin <repository-url>
```

---

## Scenario 13: Deleted File by Mistake

Solution

```bash
git restore file-name
```

---

## Scenario 14: Wrong Commit Message

Solution

```bash
git commit --amend -m "New Commit Message"
```

---

## Scenario 15: View Remote Repository

Run

```bash
git remote -v
```

Expected Output

```text
origin https://github.com/username/repository.git
```

---

## Daily Commands

```bash
git status

git branch

git switch

git add .

git commit -m "message"

git pull origin main

git push origin main

git log --oneline
```

---

## Best Practices

- Check `git status` before every commit.
- Pull the latest changes before starting work.
- Use meaningful commit messages.
- Create a feature branch for every task.
- Create a Pull Request before merging.
- Never work directly on the `main` branch.
- Delete merged branches.
- Test your code before pushing.

---

## Real-Time Company Workflow

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
Pull Request
        │
        ▼
Code Review
        │
        ▼
Merge
        │
        ▼
CI/CD Pipeline
        │
        ▼
Production Deployment
```

---

## Top 20 Git Commands

```bash
git init

git clone

git status

git add .

git commit -m "message"

git log

git log --oneline

git branch

git switch

git checkout

git merge

git rebase

git fetch

git pull

git push

git stash

git tag

git remote -v

git restore

git config --list
```

---

## Interview Tips

- Explain the complete Git workflow.
- Use real project examples.
- Mention feature branches and Pull Requests.
- Explain Merge Conflicts confidently.
- Know the difference between Merge, Rebase, Fetch, and Pull.
- Practice all commands in a local Git repository.
