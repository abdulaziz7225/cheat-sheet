# Git Reset

Suppose you've just made a couple of commits on the master branch, but you actually meant to make them on a separate branch
instead. To undo those commits, you can use `git reset`.

## Soft Reset

- `git reset --soft <commit_id>` – delete the specified commit but keep the changes in the staging area
- `git reset --soft HEAD~1` – delete the last commit but keep the changes in the staging area

## Default Reset

- `git reset <commit_id>` – delete the specified commit but keep the changes in the working directory area
- `git reset HEAD~1` – delete the last commit but keep the changes in the working directory area

## Hard Reset

- `git reset --hard <commit_id>` – both delete the specified commit and the changes from the working directory area
- `git reset --hard HEAD~1` – both delete the last commit and the changes from the working directory area
