## **1. Repository Setup & Configuration**

| Command | Description | Example |
|--------|-------------|---------|
| `git init` | Initializes a new Git repository. | `git init` |
| `git clone <url>` | Clones repository from remote. | `git clone https://github.com/user/repo.git` |
| `git config --global user.name "Name"` | Sets global username. | `git config --global user.name "Gaurav"` |
| `git config --global user.email "email@example.com"` | Sets global email. | `git config --global user.email "gaurav@example.com"` |

---

## **2. Commit & Snapshotting (Fully Combined – No Duplicates)**

| Command / Option | Description | Example |
|------------------|-------------|---------|
| `git status` | Shows working tree status. | `git status` |
| `git add <file>` | Stage a specific file. | `git add app.js` |
| `git add .` | Stage all modified/untracked files. | `git add .` |
| `git commit -m "msg"` | Commit staged changes. | `git commit -m "Initial commit"` |
| `git commit -a -m "msg"` | Auto-stage tracked files and commit. | `git commit -a -m "Quick update"` |
| `git commit --amend` | Modify previous commit. | `git commit --amend` |
| `git commit --amend --no-edit` | Amend without changing message. | `git commit --amend --no-edit` |
| `git commit --no-verify` | Skip pre-commit hooks. | `git commit --no-verify -m "skip hooks"` |

---

## **3. Branching Operations**

| Command | Description | Example |
|---------|-------------|---------|
| `git branch` | List all local branches. | `git branch` |
| `git branch <name>` | Create new branch. | `git branch feature/login` |
| `git switch <branch>` | Switch branch (recommended). | `git switch main` |
| `git checkout <branch>` | Legacy way to switch. | `git checkout develop` |
| `git checkout -b <name>` | Create + switch branch. | `git checkout -b hotfix/issue` |

---

## **4. Merging & Conflict Resolution**

| Command | Description | Example |
|---------|-------------|---------|
| `git merge <branch>` | Merge branch into current. | `git merge feature/login` |
| `git fetch` | Get updates without merging. | `git fetch` |
| `git merge --abort` | Cancel merge conflict process. | `git merge --abort` |
| `git diff` | Show differences. | `git diff main develop` |

---

## **5. Cherry-Picking**

| Command | Description | Example |
|---------|-------------|---------|
| `git cherry-pick <commit>` | Apply specific commit. | `git cherry-pick e2446fe0a` |
| `git cherry-pick --abort` | Cancel ongoing cherry-pick. | `git cherry-pick --abort` |
| `git cherry-pick --continue` | Continue after conflict. | `git cherry-pick --continue` |

---

## **6. Rebase Operations**

| Command | Description | Example |
|---------|-------------|---------|
| `git rebase <branch>` | Reapply commits on top of another branch. | `git rebase main` |
| `git rebase -i <base>` | Interactive rebase. | `git rebase -i HEAD~3` |
| `git rebase --abort` | Abort rebase. | `git rebase --abort` |
| `git rebase --continue` | Continue rebase. | `git rebase --continue` |

---

## **7. Stashing Changes**

| Command | Description | Example |
|---------|-------------|---------|
| `git stash` | Save changes temporarily. | `git stash` |
| `git stash list` | Show stashes. | `git stash list` |
| `git stash apply` | Apply stash without removing. | `git stash apply` |
| `git stash pop` | Apply and remove stash. | `git stash pop` |

---

## **8. Remote Repository Operations**

| Command | Description | Example |
|---------|-------------|---------|
| `git remote -v` | Show remote URLs. | `git remote -v` |
| `git remote add origin <url>` | Add a new remote. | `git remote add origin https...` |
| `git push` | Push commits. | `git push` |
| `git push -u origin <branch>` | Push and set upstream. | `git push -u origin develop` |
| `git pull` | Fetch + merge. | `git pull` |
| `git fetch --all` | Fetch all remotes. | `git fetch --all` |

---

## **9. Undoing Changes (Safe & Unsafe)**

| Command | Description | Example |
|---------|-------------|---------|
| `git restore <file>` | Restore working directory file. | `git restore app.py` |
| `git restore --staged <file>` | Unstage a file. | `git restore --staged app.js` |
| `git reset <file>` | Unstage / revert staged. | `git reset app.js` |
| `git reset --hard` | DANGER: Discard all local changes. | `git reset --hard` |
| `git revert <commit>` | Create new commit that reverses old one. | `git revert f3c1c0d` |
| `git clean -fd` | Remove untracked files/dirs. | `git clean -fd` |

---

## **10. Tagging**

| Command | Description | Example |
|---------|-------------|---------|
| `git tag` | List tags. | `git tag` |
| `git tag <tag>` | Lightweight tag. | `git tag v1.0` |
| `git tag -a <tag> -m "msg"` | Annotated tag. | `git tag -a v1.0 -m "Release 1.0"` |
| `git push origin <tag>` | Push tag. | `git push origin v1.0` |

---

## **11. Logs & History**

| Command | Description | Example |
|---------|-------------|---------|
| `git log` | Full commit history. | `git log` |
| `git log --oneline` | Compact view. | `git log --oneline` |
| `git show <commit>` | Details of commit. | `git show 4283ecd0` |
| `git blame <file>` | See line authorship. | `git blame index.js` |

---

## **12. Advanced Commands**

| Command | Description | Example |
|---------|-------------|---------|
| `git bisect` | Find faulty commit. | `git bisect start` |
| `git submodule update --init` | Initialize submodules. | `git submodule update --init` |
| `git reflog` | Log of HEAD changes. | `git reflog` |

---

## **13. Common Workflows**

### **Feature Branch Workflow**
| Step | Command |
|------|----------|
| Create branch | `git checkout -b feature/new-ui` |
| Commit changes | `git add . && git commit -m "UI update"` |
| Push branch | `git push -u origin feature/new-ui` |

### **Cherry-Pick Workflow**
| Step | Command |
|------|----------|
| Switch branch | `git switch release-hotfix` |
| Apply commit | `git cherry-pick <commit-id>` |

---

## **14. Submodules**

| Command | Description | Example |
|---------|-------------|---------|
| `git submodule add <url>` | Add submodule. | `git submodule add https://github.com/lib/lib.git` |
| `git submodule update --remote` | Update submodule. | `git submodule update --remote` |
| `git submodule sync` | Sync URLs. | `git submodule sync` |

---

## **15. Cleanup & Optimization**

| Command | Description | Example |
|---------|-------------|---------|
| `git gc` | Garbage collection. | `git gc` |
| `git prune` | Remove unreachable objects. | `git prune` |
| `git reflog expire --all --expire=30.days` | Cleanup old reflog. | `git reflog expire --all --expire=30.days` |

---

## **16. Git Security & Signing**

| Command | Description | Example |
|---------|-------------|---------|
| `git config --global commit.gpgsign true` | Enable signed commits. | — |
| `git tag -s <tag>` | Signed tag. | `git tag -s v1.0 -m "Signed Tag"` |
| `git verify-tag <tag>` | Verify signature. | `git verify-tag v1.0` |

---
