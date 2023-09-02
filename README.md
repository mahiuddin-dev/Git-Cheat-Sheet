# Git Cheat Sheet

## Basic Commands

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git init`                            | Initialize a new Git repository.               |
| `git clone <repository>`              | Clone a remote repository to your local machine.|
| `git add <file>`                      | Add changes in a file to the staging area.     |
| `git commit -m "message"`             | Commit staged changes with a descriptive message.|
| `git status`                          | View the status of your working directory.      |

## Configuration

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git config --global user.name "Your Name"`    | Set your global username.            |
| `git config --global user.email "youremail@example.com"` | Set your global email.           |

## Branching

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git branch`                          | List all branches in the repository.           |
| `git branch <new-branch>`             | Create a new branch.                           |
| `git branch -d <branch>`              | Delete a merged branch.                        |
| `git branch -D <branch>`              | Force delete an unmerged branch.               |
| `git checkout <branch>`               | Switch to a different branch.                  |
| `git checkout -b <new-branch>`        | Create and switch to a new branch.             |
| `git merge <branch>`                  | Merge changes from a branch into the current branch.|
| `git merge --no-ff <branch>`          | Perform a non-fast-forward merge.              |
| `git log --graph --oneline --all`     | Show a graph of the commit history for all branches. |
| `git log --left-right <branch>...<branch>` | Show commits that are unique to each branch. |
| `git log --merges <branch>..<branch>` | Show merge commits between two branches.       |

## Staged Changes

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git add <file>`                      | Add changes in a file to the staging area.     |
| `git add -p <file>`                   | Interactively stage parts of a file.           |
| `git mv <old-file> <new-file>`        | Move or rename a file.                         |
| `git rm --cached <file>`              | Unstage changes in a file.                     |
| `git rm --force <file>`               | Unstage and delete a file.                    |
| `git reset HEAD <file>`               | Unstage changes in a file.                    |
| `git reset --hard HEAD <file>`        | Unstage and delete changes in a file.         |
| `git clean -f`                        | Remove untracked files from the working tree. |
| `git clean -f -d -x`                  | Recursively remove untracked files and directories from the working tree. |


## Viewing Changes

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git diff`                            | Show changes between commits, commit and working tree, etc. |
| `git log`                             | View commit history.                           |
| `git log --oneline --graph`           | Show a compact graph of the commit history.    |
| `git log --patch`                     | Show changes introduced by each commit.       |
| `git log --decorate --graph --oneline` | Show a graph with decorations and one-line commit messages. |
| `git log --grep "pattern"`            | Search for commits with a specific message pattern. |
| `git show HEAD`                      | Display information about the latest commit.   |
| `git show HEAD^`                     | Display information about the parent of the latest commit. |
| `git blame <file>`                   | Show what revision and author last modified each line of a file. |



## Undo and History

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git checkout <commit>`               | Switch to a specific commit (detached HEAD state).|
| `git restore <file>`                  | Discard changes in the working directory.      |
| `git reset <commit>`                  | Move the current branch to a specific commit.  |
| `git reset HEAD~`                  | Undo the most recent commits  |
| `git reset --soft <commit>`           | Move the branch pointer without changing staging area. |
| `git reset --mixed <commit>`          | Move the branch pointer and reset staging area. |
| `git reset --hard <commit>`           | Move the branch pointer, staging area, and working directory. |
| `git revert <commit>`                 | Create a new commit that undoes changes from a specific commit.|
| `git cherry-pick <commit>`            | Apply a specific commit from one branch to another.|
| `git reflog`                          | View a log of all branch references.           |
| `git rebase <base-branch>`            | Reapply commits from one branch onto another.  |
| `git rebase -i <base-branch>`         | Interactive rebase (reorder, squash, edit commits). |
| `git rebase --continue`               | Continue the rebase after resolving conflicts. |
| `git rebase --interactive HEAD~3`     | Interactively rebase back to the last 3 commits. |
| `git rebase --abort`                  | Abort an ongoing rebase.                       |
| `git commit --amend -m "message"`     | Change the last commit message.        |
| `git commit --fixup <commit>`         | Create a fixup commit to be combined later.    |
| `git commit --squash <commit>`        | Combine a commit with the previous commit.     |


## Cleaning

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git clean -n`                        | List untracked files to be removed.            |
| `git clean -f`                        | Remove untracked files.                        |



## Remote Operations

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git remote`                          | List remote repositories.                      |
| `git remote -v`                       | List remote repositories and their URLs.       |
| `git remote show <remote>`            | Show information about a remote repository.    |
| `git remote add <name> <url>`         | Add a new remote repository.                   |
| `git remote rename <old-name> <new-name>` | Rename a remote repository.                |
| `git remote remove <name>`            | Remove a remote repository.                    |
| `git fetch <remote>`                  | Fetch changes from a remote repository.        |
| `git fetch <remote> <branch>`         | Fetch changes from a specific branch on a remote repository. |
| `git fetch upstream`                  | Fetch changes from the upstream repository.   |
| `git pull <remote> <branch>`          | Pull and merge changes from a remote repository. |
| `git pull --rebase <remote> <branch>` | Pull changes from a remote while rebasing your local commits. |
| `git pull --rebase --autostash <remote> <branch>` | Pull changes and auto-stash local changes. |
| `git push <remote> <branch>`          | Push local changes to a remote repository.     |
| `git push --force <remote> <branch>`  | Force push local changes to a remote repository.|
| `git push --all <remote>`             | Push all branches to a remote repository.      |
| `git push --tags <remote>`            | Push all tags to a remote repository.          |
| `git push <remote> --delete <branch>` | Delete a branch on a remote repository.        |
| `git push <remote> :<tag>`            | Delete a tag on a remote repository.           |
| `git push <remote> --tags`            | Push tags to a remote repository.              |
| `git push --set-upstream <remote> <branch>` | Set the upstream branch for the current local branch. |
| `git branch -dr <remote>/<branch>`    | Delete a remote tracking branch.               |
| `git ls-remote <remote>`              | List references in a remote repository.        |
| `git clone --mirror <repository>`     | Clone a repository as a mirrored copy.         |

## Tags

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git tag`                             | List all tags in the repository.               |
| `git tag <tag-name>`                  | Create a lightweight tag.                      |
| `git tag -a <tag-name> -m "message"`  | Create an annotated tag with a message.        |
| `git tag -d <tag-name>`               | Delete a local tag.                            |
| `git push <remote> <tag-name>`        | Push a local tag to a remote repository.       |
| `git push <remote> --tags`            | Push all local tags to a remote repository.    |
| `git show <tag-name>`                 | Display information about a tag.              |
| `git tag -l "pattern"`                | List tags that match a pattern.               |
| `git tag -a <tag-name> <commit>`      | Create a tag for a specific commit.           |
| `git tag --contains <commit>`         | List tags that contain a specific commit.     |
| `git tag -d $(git tag -l)`            | Delete all local tags.                        |
| `git push <remote> :refs/tags/<tag-name>` | Delete a remote tag.                      |


## Collaborative Work

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git fetch`                           | Download objects and refs from another repository.|
| `git pull --rebase`                   | Pull changes from a remote while rebasing your local commits.|


## Advanced

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git stash`                           | Temporarily save changes that are not ready to be committed.|
| `git submodule`                       | Manage Git submodules within your repository.  |

## Stash

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git stash`                           | Temporarily save changes that are not ready to be committed. |
| `git stash save "message"`            | Save changes to a new stash with a message.    |
| `git stash list`                      | List all stashes in the repository.            |
| `git stash show`                      | Show changes in the most recent stash.        |
| `git stash show stash@{n}`            | Show changes in a specific stash.             |
| `git stash show -p stash@{n}`         | Show changes with diff in a specific stash.   |
| `git stash apply`                     | Apply the most recent stash without removing it. |
| `git stash apply stash@{n}`           | Apply a specific stash without removing it.   |
| `git stash pop`                       | Apply and remove the most recent stash.       |
| `git stash pop stash@{n}`             | Apply and remove a specific stash.            |
| `git stash branch <branch-name>`      | Create a new branch from a stash.            |
| `git stash drop`                      | Remove the most recent stash.                |
| `git stash drop stash@{n}`            | Remove a specific stash.                     |
| `git stash clear`                     | Remove all stashes.                          |
| `git stash show -u`                   | Show untracked files in the stash.           |

## Submodules

| Command                               | Description                                     |
|---------------------------------------|-------------------------------------------------|
| `git submodule add <repository>`      | Add a new submodule to your repository.       |
| `git submodule init`                  | Initialize submodules in your repository.      |
| `git submodule update`                | Update submodules to their latest commit.     |
| `git submodule update --init`         | Initialize and update submodules.             |
| `git submodule update --remote`       | Update submodules to the latest remote commit.|
| `git submodule status`                | Show the status of submodules.                |
| `git submodule foreach <command>`     | Run a Git command in each submodule.          |
| `git submodule sync`                  | Update URLs for submodules.                  |
| `git submodule foreach --recursive <command>` | Run a Git command recursively in each submodule. |
| `git submodule add -b <branch> <repository>` | Add a submodule with a specific branch.  |
| `git submodule deinit <submodule>`    | Deinitialize a submodule.                   |
| `git submodule update --remote <submodule>` | Update a specific submodule to the latest remote commit. |
| `git submodule update --recursive`    | Update submodules and their submodules recursively. |
| `git submodule foreach --recursive git pull origin master` | Update all submodules and their nested submodules. |


**Helpful Links**

- [Git Documentation](https://git-scm.com/doc)

**Remember**: Git commands can be powerful. Always double-check before executing critical operations.
