# Detached HEAD

You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any 
commits you make in this state without impacting any branches by switching back to a branch.

## Enter detached HEAD mode

- `git checkout <commit_id>` - views a specific commit in detached HEAD mode. Only 7 digits of a commit hash is enough
- `git switch --detach <commit_id>` - same as `git checkout <commit_id>`
- `git checkout HEAD~2` - visits 2 commits before. HEAD~2 refers to 2 commits before HEAD (grandparent commit)

## Exit detached HEAD mode

- `git checkout <branch_name>` - escapes from detached HEAD mode and switches to the specified branch
- `git switch <branch_name>` - same as `git checkout <branch_name>`
- `git checkout —` - escapes from detached HEAD mode and returns to whatever previous branch was
- `git switch —` - same as `git checkout -`

## Create a new branch from a commit

- `git checkout -b <branch_name>` - creates a new branch from the specified commit
- `git switch -c <branch_name>` - same as `git checkout -b <branch_name>`
