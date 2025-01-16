# GitHub Stash

## Stash or store changes

- `git stash`
- `git stash save` - same as `git stash`
- `git stash -m "message"`

### Include untracked files in stash as well

- `git stash -u`
- `git stash --include-untracked`

## List all stashed / stored changes

- `git stash list`

## Show stash

- `git stash show` - shows the latest stash with index=0 but doesn't apply it to working directory
- `git stash show -p` - shows the latest stash including detailed differences
- `git stash show -u` - shows only untracked files of the latest stash with index=0
- `git stash show --include-untracked` - shows only untracked files of the latest stash with index=0
- `git stash show -p -u` - shows the latest stash with detailed differences including untracked files
- `git stash show -p --only-untracked` - shows the latest stash with detailed differences for only untracked files

## Apply stash

- `git stash apply` - applies the latest stash with index=0 but keeps it in the list of stashed changes
- `git stash apply stash@{1}` - applies the stash with index=1
- `git stash apply 1` - applies the stash with index=1

## Pop stash

- `git stash pop` - applies the latest stash with index=0 and deletes it from the list of stashed changes
- `git stash pop stash@{1}` - applies the stash with index=1 and deletes it from the list
- `git stash pop 1` - applies the stash with index=1 and deletes it from the list

## Drop stash

- `git stash drop` - deletes or drops the latest stash with index=0 from the list of stashed changes
- `git stash drop stash@{1}` - drops the stash with index=1
- `git stash drop 1` - drops the stash with index=1

## Delete stash list

- `git stash clear` - Clears or deletes all stashed changes

## Create branch from stash

- `git stash branch <branch_name>` - creates branch from the latest stash with index=0
- `git stash branch <branch_name> stash@{1}` - creates branch from the stash with index=1
