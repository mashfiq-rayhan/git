<h2 style="display: flex; align-items: center; justify-content: center; gap: 10px;">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git Logo" width="40">
  <span style="color:#de4c36; font-size:1.5em;">GIT</span>
</h2>

> <h4 style="color:#942917; padding:5px">01. Configuration</h4>
```sh
git config --global user.email "mashfiq.rayhan.ovi@gmail.com"  
# Sets the global email for commit authorship

git config --global user.name "mashfiq-rayhan"                
# Sets the global username for commit authorship
```

---

> <h4 style="color:#942917; padding:5px">02. Initialize Repository</h4>
```sh
git init              # Initializes a new Git repository in the current directory
```

---

> <h4 style="color:#942917; padding:5px">03. Basic Commands</h4>
```sh
git status               
# Shows the current state of the working directory and staging area

git add .               
# Stages all changes (modified and untracked files) for the next commit

git commit -m "commit message" 
# Records staged changes with a descriptive commit message

git revert <commit-id>         
# Creates a new commit to undo changes from the specified commit

git log                        
# Displays the commit history for the current branch
```

---

> <h4 style="color:#942917; padding:5px">04. Branching & Switching</h4>
```sh
git branch                       # Lists all branches in the repository
git branch <branchname>          # Creates a new branch with the specified name
git checkout <branchname>        # Switches to the specified existing branch
git checkout -b <branchname>     # Creates and switches to a new branch
git switch <branchname>          # Switches to the specified branch (modern alternative to checkout)
git switch -c <branchname>       # Creates and switches to a new branch (modern alternative)
```

---

> <h4 style="color:#942917; padding:5px">05. Merging & Rebasing</h4>
```sh
git merge <branchname>             # Merges the specified branch into the current branch
git merge --squash <branchname>    # Combines changes from the specified branch into a single commit
git commit -m "message"            # Commits merged changes with a descriptive message
git merge --no-ff <branchname>     # Merges with a merge commit, preserving branch history
git rebase <branchname>            # Reapplies current branch commits onto the specified branch
git merge --abort                  # Cancels an in-progress merge operation
```

---

> <h4 style="color:#942917; padding:5px">06. Undo Changes</h4>
```sh
git checkout <commit-id>             # Switches to a specific commit, entering a detached HEAD state
git checkout <filename>              # Restores the specified file from the last commit
git checkout .                       # Restores all files from the last commit
git restore path/<filename>          # Restores the specified file to its state in the last commit
git restore --staged <filename>      # Removes the specified file from the staging area
git reset                            # Unstages all changes, keeping them in the working directory
git reset --soft HEAD~1              # Undoes the last commit but keeps changes staged
git reset HEAD~1                     # Undoes the last commit and unstages changes
git reset --hard HEAD~1      # Undoes the last commit and discards changes in the working directory
```

---

> <h4 style="color:#942917; padding:5px">07. Deleting Branches</h4>
```sh
git branch -d <branchname>          # Deletes a fully merged branch
git branch -D <branchname>          # Forcefully deletes a branch, even if unmerged
```

---

> <h4 style="color:#942917; padding:5px">08. Stashing Changes</h4>
```sh
git stash                      # Saves uncommitted changes to a stack for later use
git stash list                 # Lists all saved stashes
git stash apply [index]        # Applies a specific stash (defaults to the latest if no index)
git stash push -m "message"    # Saves changes to a stash with a descriptive message
git stash pop [index]          # Applies and removes a specific stash from the stack
git stash drop [index]         # Deletes a specific stash from the stack
git stash clear                # Removes all stashes from the stack
```

---

> <h4 style="color:#942917; padding:5px">09. Cleaning Untracked Files</h4>
```sh
git clean -dn    # Shows untracked files that would be deleted
git clean -df    # Permanently deletes untracked files from the working directory
```

---

> <h4 style="color:#942917; padding:5px">10. Cherry-picking Commits</h4>
```sh
git cherry-pick <commit-id>    # Applies changes from a specific commit to the current branch
```

---

> <h4 style="color:#942917; padding:5px">11. Viewing Changes</h4>
```sh
git diff             # Shows differences between the working directory and staged changes
git log --merge      # Displays commits involved in a merge conflict
```

---

> <h4 style="color:#942917; padding:5px">12. Reflog & History</h4>
```sh
git reflog           # Shows a log of all reference updates (default retention: 30 days)
```

---

> <h4 style="color:#942917; padding:5px">13. Tags</h4>

> <h5 style="color:#731f12; padding:5px">Lightweight Tags</h5>
```sh
git tag <tag-id> <commit-id>     # Creates a lightweight tag pointing to a specific commit
git show <tag-id>                # Displays details of the specified tag
git tag -d <tag-id>              # Deletes the specified lightweight tag
```

> <h5 style="color:#731f12; padding:5px">Annotated Tags</h5>
```sh
git tag -a <tag-id> -m "message"     # Creates an annotated tag with a descriptive message
git tag -d <tag-id>                  # Deletes the specified annotated tag
```

---

> <h4 style="color:#942917; padding:5px">14. Local to Remote</h4>
```sh
git remote               # Lists all configured remote repositories
git branch -a               # Lists all local and remote branches
git branch -r               # Lists only remote tracking branches
git remote show origin               # Shows detailed information about the 'origin' remote
git remote add origin <repo-link>           # Adds a remote repository with the specified URL
git branch -vv                # Shows local branches and their remote tracking relationships
git push origin master               # Pushes local changes to the 'master' branch on the remote
git ls-remote               # Lists references (branches, tags) in a remote repository
git fetch origin               # Retrieves updates from the 'origin' remote without merging
git branch --track [localTrackingBranch] origin/[remoteTrackingBranch]  
# Creates a local branch tracking a remote branch
git clone <url>               # Clones a remote repository to the local machine
git branch --delete --remotes [remoteTrackingBranch] 
# Deletes a remote tracking branch locally
git push origin --delete [remoteBranch]     
# Deletes a branch on the remote repository
```

---

> <h4 style="color:#942917; padding:5px">15. Sync Forked Repository</h4>
```sh
git remote -v               # Verifies the URLs of configured remote repositories
git remote add upstream <original-repo-url>
# Adds the original repository as an upstream remote
git fetch upstream               # Retrieves updates from the upstream repository
git checkout main               # Switches to the main branch in the local repository
git merge upstream/main               # Merges upstream main branch changes into the local main branch
git push origin main                 # Pushes updated local main branch to the forked repository
```
