Git/
│
├── README.md                 ⭐ Project overview
├── 01-Basics/
├── 02-Branching/
├── 03-Collaboration/
├── 04-Advanced/
├── 05-Interview/
├── 06-Troubleshooting/
├── 07-Cheat-Sheets/
└── Images/

# Git Configuration

## Configure Username

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

## Configure Email

```bash
git config --global user.email "sanju@gmail.com"
```

Verify

```bash
git config --global user.email
```

Expected Output

```text
sanju@gmail.com
```

---

## View All Configurations

```bash
git config --list
```

Expected Output

```text
user.name=Sanju Kumar
user.email=sanju@gmail.com
```
# Create Git Repository

## Create a New Folder

```bash
mkdir git-demo
```

Verify

```bash
dir
```

Expected Output

```text
git-demo
```

---

## Move to the Project Folder

```bash
cd git-demo
```

Verify

```bash
pwd
```

Expected Output

```text
.../git-demo
```

> **Windows PowerShell:** `pwd` current location ni chupistundi.

---

## Initialize Git Repository

```bash
git init
```

Expected Output

```text
Initialized empty Git repository in .../git-demo/.git/
```

---

## Verify Git Repository

```bash
dir -Force
```

Expected Output

```text
.git
```

> **Git Bash:** `ls -la` use cheyyachu.  
> **Windows PowerShell:** `dir -Force` use cheyyi.

---

## Open Repository in VS Code

```bash
code .
```

Expected Output

```text
VS Code opens the current project.
```

---

## Check Repository Status

```bash
git status
```

Expected Output

```text
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

> **Note:** New Git versions lo `master` badulu `main` kanipinchachu.

---

## Create a File

Create a file.

```text
demo.txt
```

Add the following content.

```text
Hello Git
```

---

## Check Git Status

```bash
git status
```

Expected Output

```text
Untracked files:

demo.txt
```

---

## Stage the File

```bash
git add demo.txt
```

Verify

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: demo.txt
```

---

## Commit the File

```bash
git commit -m "Initial Commit"
```

Expected Output

```text
1 file changed
create mode 100644 demo.txt
```

---

## Verify Commit

```bash
git log --oneline
```

Expected Output

```text
<commit-id> Initial Commit
```

---

## Commands Used

```bash
mkdir git-demo

cd git-demo

git init

code .

git status

git add demo.txt

git commit -m "Initial Commit"

git log --oneline
```
# Git Basic Commands

## Check Repository Status

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Create a New File

Create a file.

```text
demo.txt
```

Add the following content.

```text
Hello Git
```

---

## Check Status

```bash
git status
```

Expected Output

```text
Untracked files:

demo.txt
```

---

## Stage a Single File

```bash
git add demo.txt
```

Verify

```bash
git status
```

Expected Output

```text
Changes to be committed:

new file: demo.txt
```

---

## Stage All Files

```bash
git add .
```

Verify

```bash
git status
```

Expected Output

```text
Changes to be committed
```

---

## Commit Changes

```bash
git commit -m "Initial Commit"
```

Expected Output

```text
1 file changed
create mode 100644 demo.txt
```

---

## Check Commit History

```bash
git log
```

Expected Output

```text
commit <commit-id>
Author: Sanju Kumar
Date: ...

Initial Commit
```

---

## Show Commit History in One Line

```bash
git log --oneline
```

Expected Output

```text
<commit-id> Initial Commit
```

---

## Modify the File

Open

```text
demo.txt
```

Add

```text
Welcome to Git
```

Save the file.

---

## Check Status

```bash
git status
```

Expected Output

```text
Changes not staged for commit:

modified: demo.txt
```

---

## View Changes

```bash
git diff
```

Expected Output

```text
+ Welcome to Git
```

---

## Stage Modified File

```bash
git add demo.txt
```

---

## Commit Modified File

```bash
git commit -m "Updated demo.txt"
```

Expected Output

```text
1 file changed
```

---

## View Commit History

```bash
git log --oneline
```

Expected Output

```text
<commit-id> Updated demo.txt
<commit-id> Initial Commit
```
---

## Commands Used

```bash
git status

git add demo.txt

git add .

git commit -m "Initial Commit"

git log

git log --oneline

git diff
```
# Git Branches

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Create a New Branch

```bash
git branch feature-login
```

Verify

```bash
git branch
```

Expected Output

```text
* main
  feature-login
```

---

## Switch to a Branch

```bash
git switch feature-login
```

Expected Output

```text
Switched to branch 'feature-login'
```

Verify

```bash
git branch
```

Expected Output

```text
  main
* feature-login
```

---

## Create and Switch to a New Branch

```bash
git switch -c feature-payment
```

Expected Output

```text
Switched to a new branch 'feature-payment'
```

Verify

```bash
git branch
```

Expected Output

```text
  main
  feature-login
* feature-payment
```

---

## Create a File

Create a file.

```text
payment.txt
```

Add the following content.

```text
Payment Module
```

---

## Check Status

```bash
git status
```

Expected Output

```text
Untracked files:

payment.txt
```

---

## Stage the File

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added payment module"
```

Expected Output

```text
1 file changed
```

---

## Switch Back to Main Branch

```bash
git switch main
```

Expected Output

```text
Switched to branch 'main'
```

Verify

```bash
git branch
```

Expected Output

```text
* main
  feature-login
  feature-payment
```

---

## List All Branches

```bash
git branch
```

Expected Output

```text
* main
  feature-login
  feature-payment
```

---

## Rename Current Branch

```bash
git branch -m payment-module
```

Verify

```bash
git branch
```

Expected Output

```text
* payment-module
  feature-login
```

---

## Delete a Branch

Switch to main.

```bash
git switch main
```

Delete the branch.

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Force Delete a Branch

```bash
git branch -D feature-login
```

---

## View Branch History

```bash
git log --oneline --graph --all
```

Expected Output

```text
* Added payment module
* Initial Commit
```

---

## Commands Used

```bash
git branch

git branch feature-login

git switch feature-login

git switch -c feature-payment

git branch -m payment-module

git switch main

git branch -d feature-login

git branch -D feature-login

git log --oneline --graph --all
```
main
   │
   ├── feature-login
   │       │
   │       ├── Code Changes
   │       ├── Commit
   │       └── Merge to Main
   │
   └── feature-payment
           │
           ├── Code Changes
           ├── Commit
           └── Merge to Main
# Git Merge

## Create a New Branch

```bash
git branch feature-login
```

Verify

```bash
git branch
```

Expected Output

```text
* main
  feature-login
```

---

## Switch to the Branch

```bash
git switch feature-login
```

Expected Output

```text
Switched to branch 'feature-login'
```

---

## Create a File

Create a file.

```text
login.txt
```

Add the following content.

```text
Login Feature
```

---

## Check Status

```bash
git status
```

Expected Output

```text
Untracked files:

login.txt
```

---

## Stage the File

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added login feature"
```

Expected Output

```text
1 file changed
```

---

## Switch to Main Branch

```bash
git switch main
```

Expected Output

```text
Switched to branch 'main'
```

---

## Check Branches

```bash
git branch
```

Expected Output

```text
* main
  feature-login
```

---

## Merge the Branch

```bash
git merge feature-login
```

Expected Output

```text
Updating xxxxxxx..xxxxxxx
Fast-forward
login.txt
```

---

## Verify Merge

```bash
git log --oneline
```

Expected Output

```text
<commit-id> Added login feature
<commit-id> Initial Commit
```

---

## Verify File

```bash
dir
```

Expected Output

```text
login.txt
demo.txt
```

---

## Delete the Merged Branch

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Verify Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## View Commit History

```bash
git log --oneline --graph
```

Expected Output

```text
* Added login feature
* Initial Commit
```

---

## Commands Used

```bash
git branch feature-login

git switch feature-login

git add .

git commit -m "Added login feature"

git switch main

git merge feature-login

git branch -d feature-login

git log --oneline

git log --oneline --graph
```
# Git Merge Conflict

## Create a New Branch

```bash
git branch feature-login
```

---

## Switch to the Branch

```bash
git switch feature-login
```

---

## Create a File

Create a file.

```text
demo.txt
```

Add the following content.

```text
Hello from Feature Branch
```

---

## Stage the File

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Updated demo.txt from feature branch"
```

---

## Switch to Main Branch

```bash
git switch main
```

---

## Modify the Same File

Open

```text
demo.txt
```

Replace the content with

```text
Hello from Main Branch
```

---

## Stage the File

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Updated demo.txt from main branch"
```

---

## Merge Feature Branch

```bash
git merge feature-login
```

Expected Output

```text
Auto-merging demo.txt
CONFLICT (content): Merge conflict in demo.txt
Automatic merge failed; fix conflicts and then commit the result.
```

---

## Check Status

```bash
git status
```

Expected Output

```text
You have unmerged paths.
```

---

## Open demo.txt

Expected Content

```text
<<<<<<< HEAD
Hello from Main Branch
=======
Hello from Feature Branch
>>>>>>> feature-login
```

---

## Resolve the Conflict

Edit the file.

```text
Hello from Main Branch
Hello from Feature Branch
```

Remove

```text
<<<<<<< HEAD
=======
>>>>>>> feature-login
```

Save the file.

---

## Stage the Resolved File

```bash
git add demo.txt
```

---

## Complete the Merge

```bash
git commit -m "Resolved merge conflict"
```

Expected Output

```text
[main xxxxxxx] Resolved merge conflict
```

---

## Verify Commit History

```bash
git log --oneline --graph
```

Expected Output

```text
*   Resolved merge conflict
|\
| * Updated demo.txt from feature branch
* | Updated demo.txt from main branch
|/
* Initial Commit
```

---

## Delete the Branch

```bash
git branch -d feature-login
```

---

## Verify Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Commands Used

```bash
git branch feature-login

git switch feature-login

git add .

git commit -m "Updated demo.txt from feature branch"

git switch main

git add .

git commit -m "Updated demo.txt from main branch"

git merge feature-login

git status

git add demo.txt

git commit -m "Resolved merge conflict"

git log --oneline --graph

git branch -d feature-login
```
# Git Remote Repository (GitHub)

## Create a New Repository in GitHub

1. Login to GitHub.
2. Click **New Repository**.
3. Enter the repository name.
4. Click **Create Repository**.

---

## Check Current Remote

```bash
git remote -v
```

Expected Output

```text
No output
```

---

## Add Remote Repository

```bash
git remote add origin https://github.com/username/git-demo.git
```

---

## Verify Remote

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/git-demo.git (fetch)
origin  https://github.com/username/git-demo.git (push)
```

---

## Rename Default Branch to Main

```bash
git branch -M main
```

Verify

```bash
git branch
```

Expected Output

```text
* main
```

---

## Push Repository to GitHub

```bash
git push -u origin main
```

Expected Output

```text
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

---

## Verify Branch Tracking

```bash
git branch -vv
```

Expected Output

```text
* main xxxxxx [origin/main]
```

---

## Show Remote Details

```bash
git remote show origin
```

Expected Output

```text
Fetch URL: https://github.com/username/git-demo.git
Push URL: https://github.com/username/git-demo.git
```

---

## Change Remote URL

```bash
git remote set-url origin https://github.com/username/new-repository.git
```

---

## Verify Updated Remote

```bash
git remote -v
```

Expected Output

```text
origin https://github.com/username/new-repository.git (fetch)
origin https://github.com/username/new-repository.git (push)
```

---

## Remove Remote

```bash
git remote remove origin
```

---

## Verify Remote Removed

```bash
git remote -v
```

Expected Output

```text
No output
```

---

## Add Remote Again

```bash
git remote add origin https://github.com/username/git-demo.git
```

---

## Verify Remote

```bash
git remote -v
```

Expected Output

```text
origin https://github.com/username/git-demo.git (fetch)
origin https://github.com/username/git-demo.git (push)
```

---

## Commands Used

```bash
git remote -v

git remote add origin https://github.com/username/git-demo.git

git branch -M main

git push -u origin main

git branch -vv

git remote show origin

git remote set-url origin https://github.com/username/new-repository.git

git remote remove origin
```
# Git Push

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Check Remote Repository

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/git-demo.git (fetch)
origin  https://github.com/username/git-demo.git (push)
```

---

## Check Repository Status

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Push Local Main Branch to GitHub

```bash
git push -u origin main
```

Expected Output

```text
Branch 'main' set up to track 'origin/main'.

Everything up-to-date
```

---

## Verify Tracking Branch

```bash
git branch -vv
```

Expected Output

```text
* main xxxxxx [origin/main]
```

---

## Modify a File

Open

```text
demo.txt
```

Add

```text
Welcome to Git Push
```

Save the file.

---

## Check Status

```bash
git status
```

Expected Output

```text
Changes not staged for commit
```

---

## Stage the Changes

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Updated demo.txt"
```

Expected Output

```text
1 file changed
```

---

## Push Latest Commit

```bash
git push
```

Expected Output

```text
Writing objects: 100%

To https://github.com/username/git-demo.git
```

---

## Create a New Branch

```bash
git switch -c feature-login
```

---

## Push New Branch

```bash
git push -u origin feature-login
```

Expected Output

```text
Branch 'feature-login' set up to track 'origin/feature-login'
```

---

## Verify Remote Branches

```bash
git branch -r
```

Expected Output

```text
origin/main
origin/feature-login
```

---

## Push All Local Branches

```bash
git push --all origin
```

---

## Delete Remote Branch

```bash
git push origin --delete feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Verify Remote Branches

```bash
git branch -r
```

Expected Output

```text
origin/main
```

---

## Force Push

```bash
git push --force
```

---

## Safe Force Push

```bash
git push --force-with-lease
```

---

## Commands Used

```bash
git remote -v

git status

git add .

git commit -m "Updated demo.txt"

git push

git push -u origin main

git switch -c feature-login

git push -u origin feature-login

git branch -r

git push --all origin

git push origin --delete feature-login

git push --force

git push --force-with-lease
```
# Git Pull

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Check Remote Repository

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/git-demo.git (fetch)
origin  https://github.com/username/git-demo.git (push)
```

---

## Check Current Status

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Pull Latest Changes from Main Branch

```bash
git pull origin main
```

Expected Output

```text
Already up to date.
```

---

## Pull Current Tracking Branch

```bash
git pull
```

Expected Output

```text
Already up to date.
```

---

## Fetch Changes Without Merging

```bash
git fetch
```

Expected Output

```text
Fetching origin
```

---

## Verify Remote Branches

```bash
git branch -r
```

Expected Output

```text
origin/main
origin/feature-login
```

---

## Pull a Specific Branch

```bash
git pull origin feature-login
```

Expected Output

```text
Updating xxxxxxx..xxxxxxx
Fast-forward
```

---

## Pull with Rebase

```bash
git pull --rebase
```

Expected Output

```text
Successfully rebased and updated refs/heads/main.
```

---

## Check Commit History

```bash
git log --oneline
```

Expected Output

```text
<commit-id> Latest Commit
<commit-id> Previous Commit
```

---

## Check Repository Status

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Commands Used

```bash
git pull

git pull origin main

git pull origin feature-login

git fetch

git pull --rebase

git branch -r

git log --oneline

git status
```
# Git Fetch

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Check Remote Repository

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/git-demo.git (fetch)
origin  https://github.com/username/git-demo.git (push)
```

---

## Fetch Latest Changes

```bash
git fetch
```

Expected Output

```text
Fetching origin
```

---

## Verify Remote Branches

```bash
git branch -r
```

Expected Output

```text
origin/main
origin/feature-login
```

---

## View Local and Remote Branches

```bash
git branch -a
```

Expected Output

```text
* main
  feature-login
  remotes/origin/main
  remotes/origin/feature-login
```

---

## Compare Local and Remote

```bash
git log HEAD..origin/main --oneline
```

Expected Output

```text
<commit-id> Latest Commit from Remote
```

---

## View File Changes

```bash
git diff main origin/main
```

Expected Output

```text
Shows the difference between local and remote.
```

---

## Fetch a Specific Branch

```bash
git fetch origin feature-login
```

Expected Output

```text
From https://github.com/username/git-demo
 * branch            feature-login -> FETCH_HEAD
```

---

## Fetch All Branches

```bash
git fetch --all
```

Expected Output

```text
Fetching origin
```

---

## Merge Fetched Changes

```bash
git merge origin/main
```

Expected Output

```text
Updating xxxxxxx..xxxxxxx
Fast-forward
```

---

## Check Repository Status

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## Commands Used

```bash
git fetch

git fetch origin feature-login

git fetch --all

git branch -r

git branch -a

git log HEAD..origin/main --oneline

git diff main origin/main

git merge origin/main

git status
```
# Git Clone

## Copy Repository URL from GitHub

Example

```text
https://github.com/username/git-demo.git
```

---

## Clone Repository

```bash
git clone https://github.com/username/git-demo.git
```

Expected Output

```text
Cloning into 'git-demo'...
Receiving objects: 100%
Resolving deltas: 100%
```

---

## Verify Repository

```bash
dir
```

Expected Output

```text
git-demo
```

---

## Move to Repository

```bash
cd git-demo
```

---

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Check Remote Repository

```bash
git remote -v
```

Expected Output

```text
origin  https://github.com/username/git-demo.git (fetch)
origin  https://github.com/username/git-demo.git (push)
```

---

## Check Repository Status

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

## Pull Latest Changes

```bash
git pull
```

Expected Output

```text
Already up to date.
```

---

## Clone into a Custom Folder

```bash
git clone https://github.com/username/git-demo.git my-project
```

Expected Output

```text
Cloning into 'my-project'...
```

---

## Move to Custom Folder

```bash
cd my-project
```

---

## Verify Current Folder

```bash
pwd
```

Expected Output

```text
.../my-project
```

---

## Clone a Specific Branch

```bash
git clone --branch feature-login https://github.com/username/git-demo.git
```

Expected Output

```text
Cloning into 'git-demo'...
```

---

## Verify Current Branch

```bash
git branch
```

Expected Output

```text
* feature-login
```

---

## Commands Used

```bash
git clone https://github.com/username/git-demo.git

git clone https://github.com/username/git-demo.git my-project

git clone --branch feature-login https://github.com/username/git-demo.git

cd git-demo

git branch

git remote -v

git status

git pull

pwd
```
# Git Pull Request

## Create a New Branch

```bash
git switch -c feature-login
```

Expected Output

```text
Switched to a new branch 'feature-login'
```

---

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* feature-login
  main
```

---

## Create a New File

Create a file.

```text
login.txt
```

Add the following content.

```text
Login Feature
```

---

## Check Status

```bash
git status
```

Expected Output

```text
Untracked files:

login.txt
```

---

## Stage the Changes

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added login feature"
```

Expected Output

```text
1 file changed
```

---

## Push Feature Branch

```bash
git push -u origin feature-login
```

Expected Output

```text
Branch 'feature-login' set up to track 'origin/feature-login'
```

---

## Open GitHub Repository

Open your GitHub repository.

Click

```text
Compare & pull request
```

---

## Create Pull Request

Enter

```text
Title:
Added Login Feature

Description:
Implemented Login Feature
```

Click

```text
Create Pull Request
```

---

## Review Pull Request

Verify

```text
Changed Files

Commits

Checks
```

---

## Merge Pull Request

Click

```text
Merge Pull Request
```

Click

```text
Confirm Merge
```

Expected Output

```text
Pull Request Successfully Merged
```

---

## Delete Remote Branch

Click

```text
Delete Branch
```

or

```bash
git push origin --delete feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Switch to Main Branch

```bash
git switch main
```

---

## Pull Latest Changes

```bash
git pull origin main
```

Expected Output

```text
Already up to date.
```

---

## Delete Local Branch

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Verify Branches

```bash
git branch
```

Expected Output

```text
* main
```

---

## Commands Used

```bash
git switch -c feature-login

git status

git add .

git commit -m "Added login feature"

git push -u origin feature-login

git switch main
# Git Rebase

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Create a New Branch

```bash
git switch -c feature-login
```

Expected Output

```text
Switched to a new branch 'feature-login'
```

---

## Create a New File

Create a file.

```text
login.txt
```

Add the following content.

```text
Login Feature
```

---

## Stage the Changes

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added login feature"
```

Expected Output

```text
1 file changed
```

---

## Switch to Main Branch

```bash
git switch main
```

---

## Modify Existing File

Open

```text
demo.txt
```

Add

```text
Updated from Main Branch
```

---

## Stage the Changes

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Updated demo.txt"
```

Expected Output

```text
1 file changed
```

---

## Switch Back to Feature Branch

```bash
git switch feature-login
```

---

## Rebase Feature Branch

```bash
git rebase main
```

Expected Output

```text
Successfully rebased and updated refs/heads/feature-login.
```

---

## Check Commit History

```bash
git log --oneline --graph
```

Expected Output

```text
* Added login feature
* Updated demo.txt
* Initial Commit
```

---

## If Rebase Conflict Occurs

```bash
git rebase main
```

Expected Output

```text
CONFLICT (content): Merge conflict in demo.txt
```

---

## Resolve the Conflict

Open

```text
demo.txt
```

Remove conflict markers.

Save the file.

---

## Stage the File

```bash
git add demo.txt
```

---

## Continue Rebase

```bash
git rebase --continue
```

Expected Output

```text
Successfully rebased and updated refs/heads/feature-login.
```

---

## Abort Rebase

```bash
git rebase --abort
```

Expected Output

```text
Rebase aborted.
```

---

## Switch to Main Branch

```bash
git switch main
```

---

## Merge Rebased Branch

```bash
git merge feature-login
```

Expected Output

```text
Fast-forward
```

---

## Delete Feature Branch

```bash
git branch -d feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Commands Used

```bash
git switch -c feature-login

git add .

git commit -m "Added login feature"

git switch main

git add .

git commit -m "Updated demo.txt"

git switch feature-login

git rebase main

git add demo.txt

git rebase --continue

git rebase --abort

git log --oneline --graph

git switch main

git merge feature-login

git branch -d feature-login
```
# Git Stash

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Modify a File

Open

```text
demo.txt
```

Add

```text
Welcome to Git Stash
```

Save the file.

---

## Check Status

```bash
git status
```

Expected Output

```text
Changes not staged for commit:

modified: demo.txt
```

---

## Stash the Changes

```bash
git stash
```

Expected Output

```text
Saved working directory and index state WIP on main
```

---

## Verify Working Directory

```bash
git status
```

Expected Output

```text
On branch main

nothing to commit, working tree clean
```

---

## View Stash List

```bash
git stash list
```

Expected Output

```text
stash@{0}: WIP on main
```

---

## Apply Stash

```bash
git stash apply
```

Expected Output

```text
Changes applied successfully.
```

---

## Verify Changes

```bash
git status
```

Expected Output

```text
Changes not staged for commit:

modified: demo.txt
```

---

## Stash Changes Again

```bash
git stash
```

---

## Apply and Remove Stash

```bash
git stash pop
```

Expected Output

```text
Dropped refs/stash@{0}
```

---

## Verify Stash List

```bash
git stash list
```

Expected Output

```text
No stash entries found.
```

---

## Create Multiple Stashes

```bash
git stash
```

```bash
git stash
```

---

## View All Stashes

```bash
git stash list
```

Expected Output

```text
stash@{0}

stash@{1}
```

---

## Apply Specific Stash

```bash
git stash apply stash@{1}
```

---

## Delete Specific Stash

```bash
git stash drop stash@{1}
```

Expected Output

```text
Dropped stash@{1}
```

---

## Delete All Stashes

```bash
git stash clear
```

Expected Output

```text
All stash entries removed.
```

---

## Verify Stash List

```bash
git stash list
```

Expected Output

```text
No stash entries found.
```

---

## Commands Used

```bash
git stash

git stash list

git stash apply

git stash pop

git stash apply stash@{1}

git stash drop stash@{1}

git stash clear

git status
```
# Git Cherry-Pick

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Create a New Branch

```bash
git switch -c feature-login
```

Expected Output

```text
Switched to a new branch 'feature-login'
```

---

## Create a New File

Create a file.

```text
login.txt
```

Add the following content.

```text
Login Feature
```

---

## Stage the Changes

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added login feature"
```

Expected Output

```text
1 file changed
```

---

## View Commit History

```bash
git log --oneline
```

Expected Output

```text
a1b2c3d Added login feature
f4g5h6i Initial Commit
```

Copy the commit id.

Example

```text
a1b2c3d
```

---

## Switch to Main Branch

```bash
git switch main
```

Expected Output

```text
Switched to branch 'main'
```

---

## Apply the Commit

```bash
git cherry-pick a1b2c3d
```

Expected Output

```text
[main xxxxxx] Added login feature
```

---

## Verify Commit History

```bash
git log --oneline
```

Expected Output

```text
xxxxxxx Added login feature
f4g5h6i Initial Commit
```

---

## Cherry-Pick Multiple Commits

```bash
git cherry-pick a1b2c3d b2c3d4e
```

Expected Output

```text
2 commits applied successfully.
```

---

## Cherry-Pick a Range of Commits

```bash
git cherry-pick a1b2c3d^..d4e5f6g
```

Expected Output

```text
All commits applied successfully.
```

---

## If Cherry-Pick Conflict Occurs

```bash
git cherry-pick a1b2c3d
```

Expected Output

```text
CONFLICT (content): Merge conflict in demo.txt
```

---

## Resolve the Conflict

Open

```text
demo.txt
```

Remove the conflict markers.

Save the file.

---

## Stage the File

```bash
git add demo.txt
```

---

## Continue Cherry-Pick

```bash
git cherry-pick --continue
```

Expected Output

```text
Cherry-pick completed successfully.
```

---

## Abort Cherry-Pick

```bash
git cherry-pick --abort
```

Expected Output

```text
Cherry-pick aborted.
```

---

## Commands Used

```bash
git switch -c feature-login

git add .

git commit -m "Added login feature"

git log --oneline

git switch main

git cherry-pick <commit-id>

git cherry-pick <commit-id1> <commit-id2>

git cherry-pick <start-commit>^..<end-commit>

git cherry-pick --continue

git cherry-pick --abort
```
# Git Tags

## Check Existing Tags

```bash
git tag
```

Expected Output

```text
No tags found.
```

---

## Create a Lightweight Tag

```bash
git tag v1.0
```

---

## Verify Tag

```bash
git tag
```

Expected Output

```text
v1.0
```

---

## Create an Annotated Tag

```bash
git tag -a v2.0 -m "Release Version 2.0"
```

---

## Verify Tags

```bash
git tag
```

Expected Output

```text
v1.0
v2.0
```

---

## View Tag Details

```bash
git show v2.0
```

Expected Output

```text
Tag: v2.0

Release Version 2.0
```

---

## Push a Specific Tag

```bash
git push origin v1.0
```

Expected Output

```text
To https://github.com/username/git-demo.git

* [new tag] v1.0 -> v1.0
```

---

## Push All Tags

```bash
git push origin --tags
```

Expected Output

```text
All tags pushed successfully.
```

---

## Delete a Local Tag

```bash
git tag -d v1.0
```

Expected Output

```text
Deleted tag 'v1.0'
```

---

## Verify Local Tags

```bash
git tag
```

Expected Output

```text
v2.0
```

---

## Delete a Remote Tag

```bash
git push origin --delete v1.0
```

Expected Output

```text
Deleted tag 'v1.0'
```

---

## Verify Remote Tag

Open GitHub Repository

Click

```text
Releases
```

Expected Output

```text
v1.0 is removed.
```

---

## Commands Used

```bash
git tag

git tag v1.0

git tag -a v2.0 -m "Release Version 2.0"

git show v2.0

git push origin v1.0

git push origin --tags

git tag -d v1.0

git push origin --delete v1.0
```

# Git Hooks

## Open Hooks Folder

```bash
cd .git/hooks
```

---

## View Available Hooks

```bash
dir
```

Expected Output

```text
applypatch-msg.sample
commit-msg.sample
pre-commit.sample
pre-push.sample
post-commit.sample
```

---

## Create Pre-Commit Hook

Create a file.

```text
pre-commit
```

---

## Add Pre-Commit Script

```sh
#!/bin/sh

echo "Running Pre-Commit Hook..."

python -m flake8 .

if [ $? -ne 0 ]
then
    echo "Flake8 Failed."
    exit 1
fi

echo "Flake8 Passed."
exit 0
```

---

## Save the File

Press

```text
Ctrl + S
```

---

## Make the Hook Executable (Linux/macOS)

```bash
chmod +x .git/hooks/pre-commit
```

---

## Create Python File

```text
demo.py
```

Add

```python
a = 5
b = 6

print(a + b)
```

---

## Stage the File

```bash
git add .
```

---

## Commit the Changes

```bash
git commit -m "Added demo.py"
```

Expected Output

```text
Running Pre-Commit Hook...

Flake8 Passed.
```

Commit Successful.

---

## Create a Flake8 Error

Open

```text
demo.py
```

Replace with

```python
a=5
b=6

print(a+b)
```

---

## Stage the File

```bash
git add .
```

---

## Commit Again

```bash
git commit -m "Testing Hook"
```

Expected Output

```text
Running Pre-Commit Hook...

Flake8 Failed.
```

Commit Blocked.

---

## Fix the Code

```python
a = 5
b = 6

print(a + b)
```

---

## Stage the File

```bash
git add .
```

---

## Commit Again

```bash
git commit -m "Fixed Flake8 Errors"
```

Expected Output

```text
Running Pre-Commit Hook...

Flake8 Passed.
```

Commit Successful.

---

## Create Commit Message Hook

Create a file.

```text
commit-msg
```

---

## Add Script

```sh
#!/bin/sh

echo "Checking Commit Message..."
```

---

## Create Pre-Push Hook

Create a file.

```text
pre-push
```

---

## Add Script

```sh
#!/bin/sh

echo "Running Pre-Push Hook..."
```

---

## Push Changes

```bash
git push
```

Expected Output

```text
Running Pre-Push Hook...
```

Push Successful.

---

## Create Post-Commit Hook

Create a file.

```text
post-commit
```

---

## Add Script

```sh
#!/bin/sh

echo "Commit Completed Successfully."
```

---

## Commit Again

```bash
git commit -m "Testing Post Commit"
```

Expected Output

```text
Commit Completed Successfully.
```

---

## Commands Used

```bash
cd .git/hooks

dir

chmod +x .git/hooks/pre-commit

git add .

git commit -m "Added demo.py"

git commit -m "Testing Hook"

git commit -m "Fixed Flake8 Errors"

git push
```
# Git Workflow (Real-Time Company Workflow)

## Developer Clones Repository

```bash
git clone https://github.com/company/project.git
```

Expected Output

```text
Repository cloned successfully.
```

---

## Move to Project Folder

```bash
cd project
```

---

## Check Current Branch

```bash
git branch
```

Expected Output

```text
* main
```

---

## Create Feature Branch

```bash
git switch -c feature-login
```

Expected Output

```text
Switched to a new branch 'feature-login'
```

---

## Develop the Feature

Create

```text
login.py
```

Add the required code.

---

## Check Status

```bash
git status
```

Expected Output

```text
Changes not staged for commit.
```

---

## Stage Changes

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Added login feature"
```

Expected Output

```text
1 file changed
```

---

## Push Feature Branch

```bash
git push -u origin feature-login
```

Expected Output

```text
Branch 'feature-login' set up to track 'origin/feature-login'
```

---

## Create Pull Request

Open GitHub Repository.

Click

```text
Compare & Pull Request
```

Click

```text
Create Pull Request
```

Expected Output

```text
Pull Request Created Successfully.
```

---

## Code Review

Reviewer checks

```text
Code Quality

Coding Standards

Security

Best Practices
```

---

## CI Pipeline Starts Automatically

Pipeline runs

```text
Lint

Unit Tests

Build

Security Scan
```

Expected Output

```text
Pipeline Passed
```

---

## Merge Pull Request

Click

```text
Merge Pull Request
```

Expected Output

```text
Pull Request Merged Successfully.
```

---

## Delete Feature Branch

```bash
git push origin --delete feature-login
```

Expected Output

```text
Deleted branch feature-login
```

---

## Pull Latest Code

```bash
git switch main
```

```bash
git pull origin main
```

Expected Output

```text
Already up to date.
```

---

## CI/CD Deployment Starts

Pipeline Deploys To

```text
Development Environment
```

Expected Output

```text
Deployment Successful.
```

---

## QA Testing

```text
QA Team Tests the Application
```

Expected Output

```text
Testing Passed.
```

---

## Deploy to UAT

```text
Deployment to UAT Environment
```

Expected Output

```text
Deployment Successful.
```

---

## User Acceptance Testing

```text
Business Team Validates the Application
```

Expected Output

```text
Approved for Production.
```

---

## Deploy to Production

```text
Production Deployment
```

Expected Output

```text
Application Live.
```

---

## Verify Production

```text
Application Working Successfully.
```

---

## Complete Workflow

```text
Clone Repository
        │
        ▼
Create Feature Branch
        │
        ▼
Write Code
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
CI Pipeline
        │
        ▼
Merge Pull Request
        │
        ▼
Deploy to Dev
        │
        ▼
QA Testing
        │
        ▼
Deploy to UAT
        │
        ▼
UAT Approval
        │
        ▼
Deploy to Production
```

---

## Commands Used

```bash
git clone https://github.com/company/project.git

cd project

git switch -c feature-login

git status

git add .

git commit -m "Added login feature"

git push -u origin feature-login

git switch main

git pull origin main

git push origin --delete feature-login
```
