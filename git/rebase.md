# Git Rebase

Brings all new commits in **main** branch to **feature** branch. Then it can be easily merged in a fast-forward approach. But is rewrites the effected commit IDs

- `git rebase <main_branch>` – rebase **main** branch to **feature** branch. Run in **feature** branch
- `git merge <feature_branch>` – merge **feature** branch to **main** branch. Run in **main** branch
- `git rebase --abort` – abort and gets back to the state before `git rebase`
- `git rebase --continue` – finish partially executed `git rebase` command

## Interactive Rebase

Running git rebase with the -i option will enter the interactive mode, which allows us to edit commits, add files, drop commits, etc. Note that we need to specify how far back we want to rewrite commits.

- `git rebase -i HEAD~<number>` – open an editor with the last `<number>` commits ex. `git rebase -i HEAD~4`

| **Commands**                 | **Description**                                                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| p, pick `<commit>`           | use commit                                                                                                                      |
| r, reword `<commit>`         | use commit, but edit the commit message                                                                                         |
| e, edit `<commit>`           | use commit, but stop for amending                                                                                               |
| s, squash `<commit>`         | use commit, but meld into previous commit                                                                                       |
| f, fixup [-C, -c] `<commit>` | like "squash" but keep only the previous commit's log message, unless -C is used, in which case keep only this commit's message |
| d, drop `<commit>`           | remove commit                                                                                                                   |

## Git Cherry Pick

Copies the changes of a specific commit in **feature** branch, then merges it to **main** branch

- `git cherry-pick <commit_id>` – copy and paste the id of commit which needs to be merged to **main** branch
