# Real-Time Git Workflow

## Objective

Learn the complete Git workflow followed by developers and DevOps engineers in real-time projects.

---

## Prerequisites

- Git Installed
- GitHub Account
- Repository Created
- Team Access Available

---

# Real-Time Company Workflow

```text
Developer
     │
     ▼
Clone Repository
     │
     ▼
Create Feature Branch
     │
     ▼
Develop Feature
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
Approve PR
     │
     ▼
Merge to Main
     │
     ▼
CI/CD Pipeline
     │
     ▼
Deployment
```

---

# Step 1: Clone Repository

Run

```bash
git clone https://github.com/username/project.git
```

---

# Step 2: Move to Project

Run

```bash
cd project
```

---

# Step 3: Check Current Branch

Run

```bash
git branch
```

Expected Output

```text
* main
```

---

# Step 4: Create Feature Branch

Run

```bash
git switch -c feature-login
```

Expected Output

```text
Switched to a new branch 'feature-login'
```

---

# Step 5: Develop Feature

Example

```bash
touch login.html
```

Modify files as required.

---

# Step 6: Check Status

Run

```bash
git status
```

---

# Step 7: Stage Changes

Run

```bash
git add .
```

---

# Step 8: Commit Changes

Run

```bash
git commit -m "Added Login Feature"
```

---

# Step 9: Push Feature Branch

Run

```bash
git push origin feature-login
```

---

# Step 10: Create Pull Request

Open GitHub

Click

```text
Compare & Pull Request
```

Fill

```text
Title

Description
```

Click

```text
Create Pull Request
```

---

# Step 11: Code Review

Reviewer checks

- Code Quality
- Coding Standards
- Security
- Best Practices

If changes are requested

Developer updates code.

```bash
git add .

git commit -m "Updated after review"

git push
```

---

# Step 12: Pull Latest Main Branch

Run

```bash
git switch main

git pull origin main
```

---

# Step 13: Merge Pull Request

Reviewer clicks

```text
Merge Pull Request
```

Expected Output

```text
Pull Request merged successfully.
```

---

# Step 14: Delete Feature Branch

Local

```bash
git branch -d feature-login
```

Remote

```bash
git push origin --delete feature-login
```

---

# Step 15: Start New Task

Run

```bash
git switch main

git pull origin main

git switch -c feature-payment
```

---

## Complete Git Workflow

```text
Clone Repository
        │
        ▼
Create Branch
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
Delete Branch
        │
        ▼
Start Next Feature
```

---

## Commands Summary

```bash
git clone <repository-url>

cd project

git branch

git switch -c feature-login

git status

git add .

git commit -m "message"

git push origin feature-login

git switch main

git pull origin main

git branch -d feature-login

git push origin --delete feature-login
```

---

## Best Practices

- Never work directly on the `main` branch.
- Create one branch for one feature.
- Pull the latest changes before starting work.
- Write meaningful commit messages.
- Create a Pull Request for every feature.
- Merge only after code review.
- Delete merged branches.

---

## Common Mistakes

### Mistake 1

Working directly on the `main` branch.

Solution

```bash
git switch -c feature-name
```

---

### Mistake 2

Forgetting to pull the latest changes.

Solution

```bash
git pull origin main
```

---

### Mistake 3

Pushing without committing.

Solution

```bash
git add .

git commit -m "message"

git push
```

---

### Mistake 4

Creating a Pull Request to the wrong branch.

Solution

Verify

```text
Base Branch = main
```

---

## Real-Time Interview Scenario

**Question**

Explain the Git workflow followed in your company.

**Answer**

```text
1. Clone the repository.

2. Create a feature branch.

3. Develop the feature.

4. Check the status.

5. Stage the changes.

6. Commit the changes.

7. Push the feature branch.

8. Create a Pull Request.

9. Reviewer reviews the code.

10. Resolve review comments if any.

11. Pull Request gets approved.

12. Merge into main branch.

13. CI/CD pipeline starts.

14. Application is deployed.

15. Delete the feature branch.
```

---

## Interview Questions

1. Explain the complete Git workflow.

2. Why do developers create feature branches?

3. Why is code review important?

4. What happens after a Pull Request is merged?

5. Why should developers avoid working on the main branch?

6. When should you pull the latest code?

7. What happens after `git push`?

8. Who approves the Pull Request?

9. What is the next step after a Pull Request is merged?

10. Which Git commands do you use daily?
