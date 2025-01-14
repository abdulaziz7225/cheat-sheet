## Git Merge

### Fast-Forward Merge

- `git merge <feature_branch>` - merges **feature** branch to **main** branch in a fast-forward approach
- `git merge --no-ff <feature_branch>` - merges **feature** branch in a recursive way

#### Squash or put all commits in feature branch into single commit and merge it to **main** branch

- `git merge --squash <feature_branch>`
- `git commit -m "message"`

### Non-Fast Forward Merge

- `git merge <feature_branch>` - merges **feature** branch to **main** branch in a recursive way

## Git Rebase

#### Brings all new commits in **main** branch to **feature** branch. Then it can be easily merged in a fast-forward approach. But is rewrites the effected commit IDs

- `git rebase <main_branch>` - rebases **main** branch to **feature** branch. Run in **feature** branch
- `git merge <feature_branch>` - merge **feature** branch to **main** branch. Run in **main** branch

## Git Cherry Pick

#### Copies the changes of a specific commit in **feature** branch, then merges it to **main** branch

- `git cherry-pick <commit_id>` - copy and paste the id of commit which needs to be merged to **main** branch