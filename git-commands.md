# Git and GitHub Commands - Complete Notes

=============================

## 1. GIT BASICS  
=============================

- git --version -> Check Git version  
- git config --global user.name "Your Name" -> Set username  
- git config --global user.email "youremail@example.com" -> Set email  
- git config --list -> Show all config details  
- git config --global core.editor "code --wait" -> Set Visual Studio Code as the default Git editor  
- git help config -> Opens the Git documentation (manual page) for config options
- git config --global -e -> Opens your global Git configuration file in the default text editor  
- git config --global color.ui auto -> Enable colored output in Git commands  
- git config --system -> Set/get a configuration value for all users on the system (requires admin/root)

## 2. INITIALIZING REPOSITORY  
=============================

-git init -> Initialize a local repository  
-git clone <url> -> Clone a remote repository

## 3. STAGING & COMMITTING  
=============================

- git status -> Check status of files  
- git add <file> -> Add specific file to staging  
- git add . -> Add all files to staging  
- git commit -m "message" -> Commit staged files with a message  
- git commit -am "message" -> Add and commit tracked files in one step  
- git add -p -> Interactive staging (review hunks)  
- git commit --amend -> Modify the last commit  
- git commit --allow-empty -> Create a commit with no changes

## 4. BRANCHING  
=============================

- git branch -> List all branches  
- git branch <name> -> Create a new branch  
- git checkout <branch> -> Switch to a branch  
- git checkout -b <branch> -> Create and switch to a new branch  
- git merge <branch> -> Merge branch into current  
- git branch -d <branch> -> Delete a branch  
- git switch <branch> -> Modern alternative to checkout  
- git switch -c <branch> -> Modern create + switch  
- git branch -vv -> Show branch tracking info

## 5. REMOTE REPOSITORIES  
=============================

- git remote -> List remotes  
- git remote -v -> Show remote URLs  
- git remote add origin <url> -> Add remote repository  
- git push -u origin main -> Push to remote main branch  
- git pull origin main -> Pull updates from remote  
- git fetch -> Fetch updates only  
- git remote rename old new -> Rename remote  
- git remote rm <name> -> Remove remote  
- git pull --rebase -> Rebase instead of merge

## 6. UNDO & RESET COMMANDS  
=============================

- git restore <file> -> Discard changes in working directory  
- git reset <file> -> Unstage a file  
- git reset --hard HEAD -> Reset all changes to last commit  
- git revert <commit> -> Revert a specific commit  
- git checkout -- <file> -> Old discard method  
- git clean -fd -> Delete untracked files and directories

## 7. VIEWING HISTORY  
=============================

- git log -> View commit history  
- git log --oneline -> Compact view of commits  
- git diff -> Show file differences  
- git show <commit> -> Show details of a commit  
- git blame <file> -> Show who modified each line  
- git log -S "text" -> Search commits by text  
- git log branch1..branch2 -> Show commits in branch2 not in branch1

## 8. GITHUB COMMANDS  
=============================

- Create a repository on GitHub via browser  
- git remote add origin <url> -> Connect local repo to GitHub  
- git push -u origin main -> Push first commit  
- git push -> Push changes  
- git pull -> Pull updates from GitHub  
- git clone <url> -> Clone GitHub repo

## 9. TAGS  
=============================

- git tag -> List tags  
- git tag -a v1.0 -m "Version 1" -> Create annotated tag  
- git push origin v1.0 -> Push tag to GitHub

## 10. IGNORING FILES  
=============================

- Create .gitignore file and list files/folders to ignore

## 11. STASHING  
=============================

- git stash -> Temporarily save uncommitted changes  
- git stash list -> List stashed changes  
- git stash pop -> Apply last stash and remove it  
- git stash apply -> Apply stash without removing it  
- git stash show -p -> Show diff of stash  
- git stash branch <name> -> Create branch from stash

## 12. ALIASES  
=============================

- git config --global alias.st status  
- git config --global alias.cm "commit -m"

## 13. COMMON SHORTCUTS  
=============================

- git diff HEAD~1 HEAD -> Compare last two commits  
- git log --graph --oneline --all -> Visual branch history  
- git fetch --all --prune -> Sync with remote branches  
- git bisect -> Find commit that introduced a bug  
- git rebase -i HEAD~n -> Interactive rebase (squash, edit, reorder)  
- git cherry-pick <commit> -> Apply specific commit

## 14. GITHUB EXTRA  
=============================

- Fork -> Copy another repo to your GitHub  
- Pull Request -> Propose changes to original repo  
- Issues -> Track bugs or requests  
- Actions -> Automate workflows

## 15. DELETE COMMANDS  
=============================

- git rm <file> -> Remove file from repo and stage  
- git rm --cached <file> -> Remove file from repo but keep local  
- git clean -f -> Remove untracked files

## 16. REFLOG & RECOVERY  
=============================

- git reflog -> Show all branch movements and commits (recover lost work)  
- git checkout <commit> -> Temporarily view an old commit

## 17. SUBMODULES  
=============================

- git submodule add <repo-url> -> Add a submodule (nested repo)  
- git submodule update --init --recursive -> Initialize and update submodules

## 18. WORKTREES  
=============================

- git worktree add ../new-worktree branch-name -> Create a linked working directory for another branch  
- git worktree list -> Show all worktrees

## 19. ADVANCED LOGGING  
=============================

- git log --graph --decorate --oneline --all -> Visualize branches and commits  
- git shortlog -sn -> Show commit count per author

## 20. PATCH & APPLY  
=============================

- git format-patch -1 <commit> -> Create a patch file from a commit  
- git apply <patchfile> -> Apply a patch file

## 21. BISECT (BUG HUNTING)  
=============================

- git bisect start -> Begin binary search for a bug  
- git bisect bad -> Mark current commit as bad  
- git bisect good <commit> -> Mark a known good commit

## 22. ADVANCED REBASE  
=============================

- git rebase -i HEAD~n -> Interactive rebase (squash, edit, reorder commits)  
- git rebase --onto <newbase> <oldbase> <branch> -> Rebase a branch onto a different base
