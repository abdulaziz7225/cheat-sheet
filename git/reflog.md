# Git Reflog

Git reflog is a rolling back 30-day storage logic. Git keeps a record of when the tips of branches and other references were updated in the repo. We can view and update these reference logs using the git reflog command

## Show all the history of last 30-day

- `git reflog show main` - views the logs for the tip of the `main` branch
- `git reflog show HEAD` - shows the log of the HEAD reference
- `git reflog HEAD` - same as `git reflog show HEAD`
- `git reflog` - same as `git reflog show HEAD`. It defaults to `HEAD`

## Reflog References

We can access specific git refs is `name@{qualifier}`. We can use this syntax to access specific ref pointers and can pass them to other commands including `checkout`, `reset`, and `merge`.

- `git reflog main@{one.week.ago}` - returns the complete log history of the `main` branch up to one week ago.
- `git checkout bugfix@{2.days.ago}` - switches to the state of the `bugfix` branch from 2 days ago
- `git diff main@{0} main@{yesterday}` - shows the differences between the current state of the `main` branch and its state as of yesterday.

## Restore a specific lost or deleted commit

- `git reset --hard <commit_id>` - writes the specified commit directly to current branch

## Restore a specific lost or deleted branch

- `git checkout <commit_id>` - checkout the commit in detached HEAD mode
- `git switch -c <branch_name>` - create a new branch from this commit
