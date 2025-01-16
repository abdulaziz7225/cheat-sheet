# Git Reflog

## Git reflog is a rolling back 30-day storage logic

### Show all the history of last 30-day

- `git reflog`

### Restore a specific lost or deleted commit

- `git reset --hard <commit_id>`

### Restore a specific lost or deleted branch

- `git checkout <commit_id>` - checkout the commit in detached HEAD mode
- `git switch -c <branch_name>` - create a new branch from this commit
