# Git Tag

## Objective

Learn how to create, view, and delete Git tags to mark important versions of a project.

---

## Prerequisites

- Git Installed
- Git Configured
- Git Repository Created
- At least one commit available

---

## Step 1: View Existing Tags

Run

```bash
git tag
```

Expected Output

```text
No tags found.
```

---

## Step 2: Create a Lightweight Tag

Run

```bash
git tag v1.0
```

Expected Output

```text
Tag created successfully.
```

---

## Step 3: Verify Tag

Run

```bash
git tag
```

Expected Output

```text
v1.0
```

---

## Step 4: Create an Annotated Tag

Run

```bash
git tag -a v1.1 -m "Version 1.1 Release"
```

Expected Output

```text
Annotated tag created successfully.
```

---

## Step 5: Verify Tag Details

Run

```bash
git show v1.1
```

Expected Output

```text
Tag: v1.1

Message: Version 1.1 Release

Commit Details...
```

---

## Step 6: Push a Single Tag

Run

```bash
git push origin v1.0
```

Expected Output

```text
To https://github.com/username/Git-Practice.git

* [new tag] v1.0 -> v1.0
```

---

## Step 7: Push All Tags

Run

```bash
git push origin --tags
```

Expected Output

```text
All tags pushed successfully.
```

---

## Step 8: Delete Local Tag

Run

```bash
git tag -d v1.0
```

Expected Output

```text
Deleted tag 'v1.0'
```

---

## Step 9: Delete Remote Tag

Run

```bash
git push origin --delete v1.0
```

Expected Output

```text
Deleted remote tag v1.0
```

---

## Real-Time Workflow

```text
Complete Feature
        │
        ▼
Testing Completed
        │
        ▼
Create Tag
        │
        ▼
git push origin --tags
        │
        ▼
Release Version
```

---

## Difference Between Lightweight and Annotated Tags

| Lightweight Tag | Annotated Tag |
|-----------------|---------------|
| Simple tag | Stores additional information |
| No message | Includes tag message |
| Less information | Includes author, date and message |
| Used for temporary marking | Used for official releases |

---

## Commands Summary

```bash
git tag

git tag v1.0

git tag -a v1.1 -m "Version 1.1 Release"

git show v1.1

git push origin v1.0

git push origin --tags

git tag -d v1.0

git push origin --delete v1.0
```

---

## Best Practices

- Use meaningful version names.
- Create tags only after successful testing.
- Use annotated tags for production releases.
- Push tags to the remote repository after creating them.

---

## Common Mistakes

### Mistake 1

Creating duplicate tags.

Error

```text
fatal: tag 'v1.0' already exists
```

Solution

```bash
git tag

git tag -d v1.0
```

---

### Mistake 2

Forgetting to push tags.

Solution

```bash
git push origin --tags
```

---

### Mistake 3

Deleting only the local tag.

Solution

Delete both local and remote tags.

```bash
git tag -d v1.0

git push origin --delete v1.0
```

---

## Real-Time Interview Scenario

**Question**

Your application has completed testing and is ready for production deployment.

How do you mark this release in Git?

**Answer**

```text
Complete Testing
        │
        ▼
Create Tag

git tag -a v1.0 -m "Production Release"

        │
        ▼
Push Tag

git push origin --tags

        │
        ▼
Production Release Completed
```

---

## Interview Questions

1. What is a Git Tag?

2. Why do we use Git Tags?

3. What is the difference between a Lightweight Tag and an Annotated Tag?

4. Which command creates an Annotated Tag?

5. How do you list all tags?

6. How do you push tags to GitHub?

7. How do you delete a local tag?

8. How do you delete a remote tag?

9. When do companies create Git Tags?

10. Why are Git Tags important in production releases?
