# GitHub Stash

## Stash or store changes

- `git stash`
- `git stash save` – same as `git stash`
- `git stash -m "message"`

### Include untracked files in stash as well

- `git stash -u`
- `git stash --include-untracked`

## List all stashed / stored changes

- `git stash list`

## Show stash

- `git stash show` – show the latest stash with index=0 but don't apply it to working directory
- `git stash show -p` – show the latest stash including detailed differences
- `git stash show -u` – show only untracked files of the latest stash with index=0
- `git stash show --include-untracked` – show only untracked files of the latest stash with index=0
- `git stash show -p -u` – show the latest stash with detailed differences including untracked files
- `git stash show -p --only-untracked` – show the latest stash with detailed differences for only untracked files

## Apply stash

- `git stash apply` – apply the latest stash with index=0 but keep it in the list of stashed changes
- `git stash apply stash@{1}` – apply the stash with index=1
- `git stash apply 1` – apply the stash with index=1

## Pop stash

- `git stash pop` – apply the latest stash with index=0 and delete it from the list of stashed changes
- `git stash pop stash@{1}` – apply the stash with index=1 and delete it from the list
- `git stash pop 1` – apply the stash with index=1 and delete it from the list

## Drop stash

- `git stash drop` – delete or drop the latest stash with index=0 from the list of stashed changes
- `git stash drop stash@{1}` – drop the stash with index=1
- `git stash drop 1` – drop the stash with index=1

## Delete stash list

- `git stash clear` – clear or delete all stashed changes

## Create branch from stash

- `git stash branch <branch_name>` – create branch from the latest stash with index=0
- `git stash branch <branch_name> stash@{1}` – create branch from the stash with index=1
