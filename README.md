Git Commands Cheat Sheet
============

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file/folder |
| `git rm -rf [file-name.txt]` | Remove a file/folder if the one above doesn't work |
| `git rm --cached [file-name.txt]` | Remove a file/folder from remote (not local) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git checkout --track origin/branchname` | Switch to a remote branch |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git stash apply` | Retrieve stash (simply |
| `git rebase -i HEAD~n` | Displays a list of the last 3 commits on the current branch (squash, pick, etc.) |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git fetch` | Downloads commits, files and branches from the git remote | 
| `git pull` | Update local repository to the newest commit (fetch + merge) |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git remote prune origin` | Removes tracked branches not on remote |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log -n 1` | View latest commit | 
| `git log --summary` | View changes (detailed) |
| `git log --name-status HEAD^..HEAD` | View files modified from last commit |
| `git diff` | Preview changes (assuming changes are not in staging/added) | 
| `git diff [source branch] [target branch]` | Preview changes before merging |

### I Messed Up
| Command | Description |
| ------- | ----------- |
| `git commit --amend -m "[commit message]"` | Change previous commit message |
| `git reset --hard origin/<branch>` | Reset local branch to origin |
| `git reset <file>` | Remove file from staging |
| `git reset` | Unstage all changes |
| `git reset HEAD~` | Undo last commit |
| `git push <remote_name> --delete <branch_name>` | Delete remote branch | 
| `git clean -fd` | Clean branch of untracked files and directories |
