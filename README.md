# Git Basics - Practice Repository

This repository is created to practice and demonstrate basic Git commands for developers, covering end-to-end daily development tasks.

---

## Steps to Set Up a Local Repository and Push to GitHub

1. **Create a local directory:**
   ```bash
   mkdir prac_git
   cd prac_git
   ```

2. **Initialize a Git repository:**
   ```bash
   git init
   ```

3. **Create a repository on GitHub:**
   - Go to [GitHub](https://github.com/) and create a new repository (e.g., `prac_git`).

4. **Link the local repo to GitHub:**
   ```bash
   git remote add origin git@github.com:vasanthreddy12/prac_git.git
   ```
   > (Use SSH or HTTPS based on your setup.)

5. **Create a `README.md` file:**
   ```bash
   touch README.md
   ```

6. **Add changes to staging:**
   ```bash
   git add .
   ```

7. **Commit the changes:**
   ```bash
   git commit -m "Initial commit"
   ```

8. **Push to GitHub:**
   ```bash
   git push origin main
   ```

---

## Daily Git Commands for Developers

| Command | Description |
|:--------|:------------|
| `git clone <url>` | Clone an existing repository |
| `git status` | Show the working tree status |
| `git add .` | Stage all modified and new files |
| `git commit -m "message"` | Commit changes with a message |
| `git push origin <branch>` | Push commits to remote branch |
| `git pull origin <branch>` | Pull latest changes from remote |
| `git fetch` | Fetch updates from remote (without merging) |
| `git branch` | List local branches |
| `git branch <branch-name>` | Create a new branch |
| `git checkout <branch-name>` | Switch to a branch |
| `git checkout -b <branch-name>` | Create and switch to a new branch |
| `git merge <branch-name>` | Merge a branch into the current branch |
| `git stash` | Temporarily save changes without committing |
| `git stash pop` | Reapply stashed changes |
| `git log --oneline` | View a compact commit history |
| `git diff` | View changes not yet staged |
| `git diff --staged` | View changes staged for commit |
| `git remote -v` | View remote repositories |
| `git rebase <branch>` | Reapply commits on top of another branch |
| `git reset --hard <commit-id>` | Reset to a specific commit (destructive) |
| `git revert <commit-id>` | Create a new commit that reverts an old one |
| `git cherry-pick <commit-id>` | Apply a specific commit onto current branch |
| `git tag <tagname>` | Create a new tag |
| `git push origin --tags` | Push all tags to remote |

---

## Common Git Workflows

### Create and Work on a New Feature Branch
```bash
git checkout -b feature/my-new-feature
# make changes
git add .
git commit -m "Add my new feature"
git push origin feature/my-new-feature
```

### Update Local Branch with Remote Changes
```bash
git pull origin main
```

or if using **rebase** to avoid unnecessary merge commits:
```bash
git pull --rebase origin main
```

### Merge Feature Branch into Main
```bash
git checkout main
git pull origin main
git merge feature/my-new-feature
git push origin main
```

### Fix a Merge Conflict
- After a merge conflict appears:
```bash
# Edit conflicted files to resolve
git add <resolved-file>
git commit
```

---

## Notes

- Always **commit meaningful messages**.
- Always **pull** the latest changes before starting work.
- Use **branches** for features, bug fixes, experiments.
- Keep your **main** (or **master**) branch clean and production-ready.
- **Rebase carefully** (only if you know what you are doing) — otherwise, stick to merge.

---

> ✨ **Tip:** Set your default branch name globally if needed:
> ```bash
> git config --global init.defaultBranch main
> ```

---

# Quick Cheat Sheet

```bash
git clone <url>           # Clone project
git checkout -b <branch>  # Create and checkout new branch
git add .                 # Stage all changes
git commit -m "message"   # Commit changes
git push origin <branch>  # Push branch to remote
git pull origin <branch>  # Pull changes
git merge <branch>        # Merge another branch into current
git stash                 # Save uncommitted changes
git stash pop             # Reapply stashed changes
git log --oneline         # Short commit history
```

---

# Happy Coding! 🚀
