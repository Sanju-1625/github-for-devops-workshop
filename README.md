# Pre-Commit Hook with Flake8

## Step 1: Create a New Project Folder

Open VS Code Terminal.

```bash
mkdir pre-commit-demo
```

Move to the project folder.

```bash
cd pre-commit-demo
```

Initialize a Git repository.

```bash
git init
```

Open the project in VS Code.

```bash
code .
```

---

## Step 2: Create a Python File

Create a file named:

```text
demo.py
```

Add the following code.

```python
a = 5
b = 6

c = a + b

print(c)
```

Run the file.

```bash
python demo.py
```

Expected Output:

```text
11
```

---

## Step 3: Install Flake8

Install Flake8.

```bash
python -m pip install flake8
```

Verify the installation.

```bash
python -m flake8 --version
```

If a version is displayed, Flake8 is installed successfully.

---

## Step 4: Create the Pre-Commit Hook

Open the hooks folder.

```bash
code .git/hooks
```

Create a new file.

```text
pre-commit
```

**Important:**

Correct:

```text
pre-commit
```

Wrong:

```text
pre_commit
pre-commit.txt
```

---

## Step 5: Add the Hook Script

Open the `pre-commit` file and paste the following script.

```sh
#!/bin/sh

echo "Running Flake8..."

python -m flake8 .

if [ $? -ne 0 ]
then
    echo "Flake8 Failed."
    exit 1
fi

echo "Flake8 Passed."
exit 0
```

Save the file.

---

## Step 6: Test the Hook

Modify `demo.py` with a style error.

```python
a=5
b=6

print(a+b)
```

Stage the file.

```bash
git add .
```

Commit the changes.

```bash
git commit -m "test"
```

Expected Output:

```text
Running Flake8...
Flake8 Failed.
```

The commit is blocked.

---

## Step 7: Fix the Code

Correct the code.

```python
a = 5
b = 6

print(a + b)
```

Stage the changes again.

```bash
git add .
```

Commit again.

```bash
git commit -m "fixed"
```

Expected Output:

```text
Running Flake8...
Flake8 Passed.
```

The commit is successful.

---

# Complete Flow

```text
Create Project Folder
        │
        ▼
git init
        │
        ▼
Create demo.py
        │
        ▼
Install Flake8
        │
        ▼
Create pre-commit Hook
        │
        ▼
Add Hook Script
        │
        ▼
git add .
        │
        ▼
git commit
        │
        ▼
Pre-Commit Hook Runs
        │
        ▼
Flake8 Checks Code
        │
   ┌────┴────┐
   │         │
 Pass      Fail
   │         │
   ▼         ▼
Commit    Commit Blocked
```

# Commands Used

```bash
mkdir pre-commit-demo
cd pre-commit-demo
git init
code .

python demo.py

python -m pip install flake8
python -m flake8 --version

code .git/hooks

git add .
git commit -m "test"
git commit -m "fixed"
```
