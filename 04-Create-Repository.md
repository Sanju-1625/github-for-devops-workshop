# Create Git Repository

## Objective

Learn how to create a new Git repository and verify it.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Bash Open

---

## Step 1: Create a Project Folder

Run

```bash
mkdir Git-Practice
```

Verify

```bash
ls
```

Expected Output

```text
Git-Practice
```

---

## Step 2: Navigate to the Project Folder

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

## Step 3: Initialize Git Repository

Run

```bash
git init
```

Expected Output

```text
Initialized empty Git repository in ...
```

---

## Step 4: Verify Hidden Files

Run

```bash
ls -la
```

Expected Output

```text
.git
```

The `.git` folder confirms that the repository has been created successfully.

---

## Step 5: Check Repository Status

Run

```bash
git status
```

Expected Output

```text
On branch main

No commits yet

nothing to commit
```

---

## Step 6: Create Your First File

Run

```bash
touch README.md
```

Verify

```bash
ls
```

Expected Output

```text
README.md
```

---

## Step 7: Check Status Again

Run

```bash
git status
```

Expected Output

```text
Untracked files:

README.md
```

---

## Repository Structure

```text
Git-Practice/
│
├── .git/
└── README.md
```

---

## Commands Summary

```bash
mkdir Git-Practice

cd Git-Practice

git init

ls -la

git status

touch README.md

ls
```

---

## Interview Questions

1. What is a Git Repository?

2. Which command creates a Git repository?

3. What is the purpose of the `.git` folder?

4. How do you verify that a repository has been created successfully?

5. What does `git status` show after creating a new repository?
