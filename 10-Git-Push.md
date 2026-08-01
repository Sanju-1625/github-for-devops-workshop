# Git Push

## Objective

Learn how to upload local commits from your Git repository to a remote GitHub repository.

---

## Prerequisites

- Git Installed
- Git Configured
- GitHub Account
- GitHub Repository Created
- Local Repository Created
- At least one commit available

---

## Step 1: Check Repository Status

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

## Step 2: Verify Remote Repository

Run

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/Git-Practice.git (fetch)

origin  https://github.com/username/Git-Practice.git (push)
```

---

## Step 3: Push Code to GitHub

Run

```bash
git push origin main
```

Expected Output

```text
Enumerating objects...

Counting objects...

Writing objects...

To https://github.com/username/Git-Practice.git

main -> main
```

---

## Step 4: Verify on GitHub

Open GitHub Repository.

Refresh the page.

Expected Output

```text
Latest commit should be visible.
```

---

## Step 5: Modify a File

Run

```bash
echo "Git Push Practice" >> README.md
```

---

## Step 6: Check Status

Run

```bash
git status
```

Expected Output

```text
Changes not staged for commit
```

---

## Step 7: Stage Changes

Run

```bash
git add .
```

---

## Step 8: Commit Changes

Run

```bash
git commit -m "Updated README"
```

Expected Output

```text
[main xxxxxx] Updated README
```

---

## Step 9: Push Latest Commit

Run

```bash
git push origin main
```

Expected Output

```text
To https://github.com/username/Git-Practice.git

main -> main
```

---

## Real-Time Workflow

```text
Developer Changes Code
        │
        ▼
git status
        │
        ▼
git add .
        │
        ▼
git commit -m "message"
        │
        ▼
git push origin main
        │
        ▼
Code Available on GitHub
```

---

## Commands Summary

```bash
git remote -v

git status

git add .

git commit -m "message"

git push origin main
```

---

## Best Practices

- Always check `git status` before pushing.
- Commit your changes before pushing.
- Write meaningful commit messages.
- Push only tested code.
- Pull the latest changes before pushing if working in a team.

---

## Common Mistakes

### Mistake 1

Trying to push without committing.

Error

```text
Everything up-to-date
```

Solution

```bash
git add .

git commit -m "Your commit message"

git push origin main
```

---

### Mistake 2

Remote Repository Not Added

Error

```text
fatal: No configured push destination
```

Solution

```bash
git remote add origin <repository-url>
```

---

### Mistake 3

Authentication Failed

Error

```text
Authentication failed
```

Solution

Use your GitHub Personal Access Token (PAT) or configure SSH authentication.

---

### Mistake 4

Push Rejected

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

## Interview Questions

1. What is Git Push?

2. Why do we use `git push`?

3. Which command uploads local commits to GitHub?

4. What is the difference between `git commit` and `git push`?

5. Why does `git push` fail sometimes?

6. How do you verify that the code has been pushed successfully?

7. What is the purpose of `origin` in `git push origin main`?
