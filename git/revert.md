# Git Revert

`git revert` is similar to `git reset` in that they both "undo" changes, but they accomplish it in different ways.

`git reset` actually moves the branch pointer backwards, eliminating commits.

`git revert` instead creates a brand new commit which reverses/undos the changes from a commit. Because it results in a new commit, you will be prompted to enter a commit message

- `git revert <commit_id>` – create a brand new commit which reverses/undos the changes from the specified commit
- `git revert HEAD~2` – create a brand new commit which reverses/undos the changes from the 2 commits before HEAD
