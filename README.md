# Git Labs – SSH Key, Commits, Reset & Revert

This lab demonstrates Git operations including SSH key setup, repository initialization, commits, branch management, hard resets, and reverts.

---

## Steps Performed

- **SSH Key Setup**
  - Generate SSH key: `ssh-keygen -t ed25519 -C "doniasobhyhelmy@gmail.com"`
  - Add key to SSH agent: `ssh-add ~/.ssh/id_ed25519`

- **Repository Initialization**
  - Create project folder: `mkdir Git_labs`
  - Move into folder: `cd Git_labs`
  - Initialize Git repo: `git init`
  - Configure Git user:
    - `git config user.name "donia sobhy"`
    - `git config user.email "doniasobhyhelmy@gmail.com"`

- **First Commit**
  - Create a file: `echo "donia sobhy helmy" > myname.txt`
  - Stage changes: `git add .`
  - Commit: `git commit -m "Adding my name"`

- **Branching & Remote**
  - Rename branch to main: `git branch -M main`
  - Add remote repository: `git remote add origin git@github.com:doniasobhyhelmy-gif/Git_labs.git`
  - Push to GitHub: `git push -u origin main`

- **Sequential Commits**
  - Append changes and commit multiple times:
    - `echo "Change 1" >> myname.txt` → `git add .` → `git commit -m "commit 1"`
    - `echo "Change 2" >> myname.txt` → `git add .` → `git commit -m "commit 2"`
    - `echo "Change 3" >> myname.txt` → `git add .` → `git commit -m "commit 3"`
    - `echo "Change 4" >> myname.txt` → `git add .` → `git commit -m "commit 4"`

- **Hard Reset**
  - Remove last 2 commits: `git reset --hard HEAD~2`
  - Append new change and commit: `echo "Step after deletion" >> myname.txt` → `git add .` → `git commit -m "commit after deletion"`

- **Final Commits**
  - Append lab completion note: `echo "lab is done" >> myname.txt` → `git add .` → `git commit -m "lab done"`
  - Amend last commit: `echo "finish" >> myname.txt` → `git add .` → `git commit -m ---amend "finish"`

- **Revert Commits (Bonus)**
  - Revert last 3 commits without committing immediately: `git revert --no-commit HEAD HEAD~1 HEAD~2`
  - Commit the revert: `git commit -m " Revert last 3 commits"`

- **Push Final Changes**
  - Push all changes to GitHub: `git push -u origin main`

---

This lab covers **key Git operations**:
- SSH key setup
- Repo initialization
- Adding, committing, amending files
- Branch management
- Hard reset
- Reverting commits
- Pushing to GitHub
