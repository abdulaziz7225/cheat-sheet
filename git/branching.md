# Git Branching

## List Branch

- `git branch` – list all branches available
- `git branch -r` – list all remote branches available
- `git branch -a` – list all local and remote branches available
- `git branch -v` – list all branches including the hash value and message of last commit in these repositories

## Create, Rename and Delete Branch

- `git branch <new_branch_name>` – create a new branch but HEAD still stays pointing to current branch
- `git branch -d <branch_name>` – delete a branch only after it has been fully merged in its upstream branch
- `git branch -D <branch_name>` – delete a branch forcefully even though it hasn't been merged to its upstream branch
- `git branch -m <branch_name>` – move / rename a branch, together with its config and reflog
- `git branch -M <branch_name>` – move / rename a branch. `-M` flag is a shortcut for `--move --force`

## Git Switch

The git switch command was introduced in Git 2.23

- `git switch <branch_name>` – switch HEAD pointer to the specified branch
- `git switch -c <new_branch_name>` – create a new branch AND switch to it all in one go

When there are unstaged changes or files, the `git switch <branch_name>` command usually does one of two things:

1. If the changes conflict with the target branch, it returns an error, warning that the changes will be lost if you proceed. In this case, you need to commit or stash the changes before switching branches.
2. If there is no conflict between the branches, the command carries over all unstaged changes to the target branch seamlessly.

## Git Checkout

Historically, we used `git checkout <branch-name>` to switch branches. This still works. The checkout command does a million additional things, so the decision was made to add a standalone switch command which is much simpler.

- `git checkout <branch_name>` – switch HEAD pointer to the specified branch
- `git checkout -b <new_branch_name>` – create a new branch AND switches to it all in one go
- `git checkout <remote>/<branch_name>` – ex. `git checkout origin/feature1`
