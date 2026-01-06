# Other Git related useful information

## How to `git commit` with the previous date?

```bash
GIT_COMMITTER_DATE="2026-04-12 10:05:22 +0100" git commit --date="2026-04-12 10:05:22 +0100" -m "Solve 1446. Consecutive Characters"
```

Update the last 3 commit messages while keeping the timestamps (both Author Date and Committer Date) looking like the originals

```bash
git rebase -i HEAD~3 --committer-date-is-author-date
```
