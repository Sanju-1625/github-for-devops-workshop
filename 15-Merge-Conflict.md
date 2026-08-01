# Merge Conflict

## Objective

Learn how to create and resolve a Git Merge Conflict.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one commit available
- Two branches available

---

## Step 1: Check Current Branch

Run

```bash
git branch
```

Expected Output

```text
* main
feature-login
```

---

## Step 2: Switch to Feature Branch

Run

```bash
git switch feature-login
```

Expected Output

```text
Switched to branch 'feature-login'
```

---

## Step 3: Modify README.md

Run

```bash
echo "Login Feature" >> README.md
```

---

## Step 4: Stage the Changes

Run

```bash
git add .
```

---

## Step 5: Commit the Changes

Run

```bash
git commit -m "Updated README from feature branch"
```

Expected Output

```text
[feature-login xxxxxx] Updated README from feature branch
```

---

## Step 6: Switch to Main Branch

Run

```bash
git switch main
```

---

## Step 7: Modify the Same File

Run

```bash
echo "Main Branch Update" >> README.md
```

---

## Step 8: Stage the Changes

Run

```bash
git add .
```

---

## Step 9: Commit the Changes

Run

```bash
git commit -m "Updated README from main branch"
```

Expected Output

```text
[main xxxxxx] Updated README from main branch
```

---

## Step 10: Merge Feature Branch

Run

```bash
git merge feature-login
```

Expected Output

```text
Auto-merging README.md

CONFLICT (content): Merge conflict in README.md

Automatic merge failed; fix conflicts and then commit the result.
```

---

## Step 11: Check Status

Run

```bash
git status
```

Expected Output

```text
You have unmerged paths.
```

---

## Step 12: Open README.md

Expected Output

```text
<<<<<<< HEAD

Main Branch Update

=======

Login Feature

>>>>>>> feature-login
```

---

## Step 13: Resolve Conflict

Edit the file.

Keep the required content.

Example

```text
Main Branch Update

Login Feature
```

Remove

```text
<<<<<<< HEAD

=======

>>>>>>> feature-login
```

Save the file.

---

## Step 14: Stage Resolved File

Run

```bash
git add README.md
```

---

## Step 15: Commit Merge

Run

```bash
git commit -m "Resolved merge conflict"
```

Expected Output

```text
[main xxxxxx] Resolved merge conflict
```

---

## Step 16: Verify

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

## Step 17: View Commit History

Run

```bash
git log --oneline
```

Expected Output

```text
Resolved merge conflict

Updated README from feature branch

Updated README from main branch
```

---

## Real-Time Workflow

```text
Developer 1
        │
        ▼
Modify README.md
        │
        ▼
Commit Changes

                GitHub

Developer 2
        │
        ▼
Modify Same README.md
        │
        ▼
Commit Changes
        │
        ▼
Merge
        │
        ▼
Merge Conflict
        │
        ▼
Resolve Conflict
        │
        ▼
Commit
```

---

## Commands Summary

```bash
git switch feature-login

git add .

git commit -m "Updated README"

git switch main

git merge feature-login

git status

git add README.md

git commit -m "Resolved merge conflict"

git log --oneline
```

---

## Best Practices

- Pull the latest code before starting work.
- Avoid editing the same file as another developer.
- Resolve conflicts carefully.
- Test the application after resolving conflicts.
- Commit only after resolving all conflicts.

---

## Common Mistakes

### Mistake 1

Committing before resolving the conflict.

Error

```text
Committing is not possible because you have unmerged files.
```

Solution

```bash
Resolve Conflict

git add README.md

git commit -m "Resolved merge conflict"
```

---

### Mistake 2

Deleting valid code while resolving the conflict.

Solution

Review both changes carefully before saving the file.

---

### Mistake 3

Leaving conflict markers in the file.

Wrong

```text
<<<<<<< HEAD
=======
>>>>>>> feature-login
```

Solution

Remove all conflict markers before committing.

---

## Real-Time Interview Scenario

**Question**

Two developers modified the same file.

Developer 1 changed line 10.

Developer 2 also changed line 10.

When merging the branches, Git shows a merge conflict.

What should you do?

**Answer**

```text
Open the conflicted file
        │
        ▼
Review both changes
        │
        ▼
Keep the required code
        │
        ▼
Remove conflict markers
        │
        ▼
Save the file
        │
        ▼
git add README.md
        │
        ▼
git commit -m "Resolved merge conflict"
```

---

## Interview Questions

1. What is a Merge Conflict?

2. Why does a Merge Conflict occur?

3. How do you identify a Merge Conflict?

4. How do you resolve a Merge Conflict?

5. Which command shows files with conflicts?

6. Why should conflict markers be removed?

7. What should you do after resolving a conflict?

8. Can Git resolve all merge conflicts automatically?

9. What is the purpose of `git add` after resolving a conflict?

10. How do you verify that the conflict has been resolved?
