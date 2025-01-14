## Git Diff

`git diff` command is used to view changes between commits, branches, files, our working directory, and more

- `git diff` - lists all the changes in our working directory that are **NOT** staged for the next commit
- `git diff HEAD` - lists all changes in the working tree including **staged** and **unstaged** files since the last commit
- `git diff --staged` - lists all the changes between the ONLY **staging** area and our last commit
- `git diff --cached` - returns the same output as `git diff --staged`

### Git Diff for specific file or files

- `git diff HEAD <file_name>` - returns all the changes related to this specific file
- `git diff --staged <file_name>`
- `git diff --staged <file_name_1> <file_name_2>`

### Comparing Branches

Order of branches in `git diff` is important for the output

- `git diff <branch_1>..<branch_2>` - list the changes between the tips of <branch_1> and <branch_2>
- `git diff <branch_1> <branch_2>` - returns the same output as `git diff <branch_1>..<branch_2>`

### Comparing Commits

Order of commit IDs in `git diff` is important for the output

- `git diff <commit_1>..<commit_2>` - list the changes between the tips of <commit_1> and <commit_2>
- `git diff <commit_1> <commit_2>` - returns the same output as `git diff <commit_1>..<commit_2>`
