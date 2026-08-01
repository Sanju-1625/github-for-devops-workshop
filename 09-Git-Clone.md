# Git Clone

## Objective

Learn how to copy an existing remote Git repository to your local machine.

---

## Prerequisites

- Git Installed
- Git Configured
- GitHub Account
- Existing GitHub Repository

---

## Step 1: Copy Repository URL

Open GitHub.

Open your repository.

Click **Code**.

Copy the HTTPS URL.

Example

```text
https://github.com/username/Git-Practice.git
```

---

## Step 2: Open Git Bash

Navigate to the location where you want to download the repository.

Run

```bash
cd Desktop
```

Verify

```bash
pwd
```

Expected Output

```text
Desktop
```

---

## Step 3: Clone Repository

Run

```bash
git clone https://github.com/username/Git-Practice.git
```

Expected Output

```text
Cloning into 'Git-Practice'...

Receiving objects: 100%

Resolving deltas: 100%
```

---

## Step 4: Verify Repository

Run

```bash
ls
```

Expected Output

```text
Git-Practice
```

---

## Step 5: Navigate to Repository

Run

```bash
cd Git-Practice
```

Verify

```bash
pwd
```

Expected Output

```text
Current directory should be Git-Practice
```

---

## Step 6: Verify Repository Status

Run

```bash
git status
```

Expected Output

```text
On branch main

Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

## Step 7: Verify Remote Repository

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

## Repository Structure

```text
Git-Practice/
│
├── .git/
├── README.md
├── index.html
└── style.css
```

---

## Commands Summary

```bash
git clone <repository-url>

git status

git remote -v

ls

cd Git-Practice

pwd
```

---

## Best Practices

- Always clone using the correct repository URL.
- Clone the repository only once.
- Verify the remote repository using `git remote -v`.
- Check `git status` after cloning.

---

## Common Mistakes

### Mistake 1

Wrong Repository URL

Error

```text
Repository not found
```

Solution

Copy the correct repository URL from GitHub.

---

### Mistake 2

No Permission

Error

```text
Permission denied
```

Solution

Ensure you have access to the repository.

---

### Mistake 3

Internet Connection Issue

Error

```text
Failed to connect
```

Solution

Check your internet connection and try again.

---

## Interview Questions

1. What is Git Clone?

2. Why do we use `git clone`?

3. Which command is used to clone a repository?

4. What is the difference between `git init` and `git clone`?

5. How do you verify the remote repository?

6. What is the purpose of `git remote -v`?

7. What happens after running `git clone`?
