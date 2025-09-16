# Git Merge

To merge, follow these basic steps:

1. Switch to or checkout the branch you want to merge the changes into (the receiving branch)
2. Use the git merge command to merge changes from a specific branch into the current branch.

## Fast-Forward Merge

- `git merge <feature_branch>` – merge **feature** branch to **main** branch in a fast-forward approach
- `git merge --no-ff <feature_branch>` – merge **feature** branch in a recursive way

### Squash or put all commits in feature branch into single commit and merge it to **main** branch

- `git merge --squash <feature_branch>`
- `git commit -m "message"`

## Non-Fast Forward Merge

- `git merge <feature_branch>` – merge **feature** branch to **main** branch in a recursive way
