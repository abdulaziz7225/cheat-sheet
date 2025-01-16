# Git Reset

Suppose you've just made a couple of commits on the master branch, but you actually meant to make them on a separate branch
instead. To undo those commits, you can use `git reset`.

## Soft Reset

- `git reset --soft <commit_id>` - deletes the specified commit but keeps the changes in the staging area
- `git reset --soft HEAD~1` - deletes the last commit but keeps the changes in the staging area

## Default Reset

- `git reset <commit_id>` - deletes the specified commit but keeps the changes in the working directory area
- `git reset HEAD~1` - deletes the last commit but keeps the changes in the working directory area

## Hard Reset

- `git reset --hard <commit_id>` - both deletes the specified commit and the changes from the working directory area
- `git reset --hard HEAD~1` - both deletes the last commit and the changes from the working directory area
