# Git Configuration

## Objective

Learn how to configure Git with your username and email.

---

## Prerequisites

- Git Installed
- Git Bash Open

---

## Step 1: Check Existing Configuration

Run

```bash
git config --list
```

Expected Output

```text
Displays the current Git configuration.
```

---

## Step 2: Configure Username

Run

```bash
git config --global user.name "Sanju Kumar"
```

Verify

```bash
git config --global user.name
```

Expected Output

```text
Sanju Kumar
```

---

## Step 3: Configure Email

Run

```bash
git config --global user.email "sanju@example.com"
```

Verify

```bash
git config --global user.email
```

Expected Output

```text
sanju@example.com
```

Replace it with your GitHub email address.

---

## Step 4: Set Default Branch Name

Run

```bash
git config --global init.defaultBranch main
```

Verify

```bash
git config --global init.defaultBranch
```

Expected Output

```text
main
```

---

## Step 5: Verify All Configuration

Run

```bash
git config --list
```

Expected Output

```text
user.name=Sanju Kumar
user.email=sanju@example.com
init.defaultBranch=main
...
```

---

## Commands Summary

```bash
git config --list

git config --global user.name "Sanju Kumar"

git config --global user.email "sanju@example.com"

git config --global init.defaultBranch main

git config --global user.name

git config --global user.email

git config --global init.defaultBranch
```

---

## Interview Questions

1. Why do we configure Git?

2. Which command is used to configure the username?

3. Which command is used to configure the email?

4. How do you verify Git configuration?

5. What is the purpose of the `--global` option?
