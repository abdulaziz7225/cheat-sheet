# Git Push

Imagine now we have a remote set up, let's push some work up to Github! To do this, we need to use the git push command.
We need to specify the remote we want to push up to AND the specific local branch we want to push up to that remote

- `git push <remote> <local_branch>:<remote_branch>` – connect a local branch with a different remote branch (ex. `git push origin feature1:feature2`)
- `git push <remote> <branch>` – set the same name for remote repository as local one (ex.`git push origin main`)
- `git push --set-upstream <remote> <branch>` – push the changes to remote repository and remember its name for the next usages
- `git push -u <remote> <branch>` – same as `git push --set-upstream <remote> <branch>`
