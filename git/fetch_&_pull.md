# Fetching and Pulling

- `git checkout --track origin/<branch_name>` – create a new local branch from the remote branch of the same name AND sets it up to track the remote branch `origin<branch_name>`
- `git switch <branch_name>` – same as `git checkout --track origin/<branch_name>`

## Git Fetch

Fetching allows us to download changes from a remote repository, BUT those changes will not be automatically integrated
into our working files. It lets you see what others have been working on, without having to merge those changes into your
local repo.

- `git fetch <remote>` – fetch all changes from a specific remote repository. If not specified, `<remote>` defaults to `origin` (ex. `git fetch origin`)
- `git fetch origin <branch_name>` – fetch only a specific branch from a remote repository

## Git Pull

`git pull` is another command we can use to retrieve changes from a remote repository. Unlike `fetch`, `pull` actually updates our HEAD branch with whatever changes are retrieved from the remote.

- `git pull` = `git fetch` + `git merge`
- `git pull <remote> <branch_name>` – fetch the latest information from the remote `<branch_name` and merges those changes into our current branch (ex. `git pull origin feature`)
- `git pull` – `<remote`> will default to `origin`, `<branch_name>` will default to whatever tracking connection is configured for the current local branch
