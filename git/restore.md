# Discarding Changes

The `git restore` command was introduced in Git 2.23

## Git Checkout

- `git checkout HEAD <file_name>` – discard any changes in that file, reverting back to the HEAD
- `git checkout -- <file_name>` – same as `git checkout HEAD <file_name>`
- `git checkout HEAD <file1> <file2> <file3>` – work with multiple files as well

## Git Restore

- `git restore --source HEAD~1 <file_name>` – restore the file to the contents in the HEAD (last commit)
- `git restore --source HEAD~2 <file_name>` – restore the file to the contents of 2 commits before HEAD (grandparent commit)
- `git restore <file_name>` – same as `git restore --source HEAD~1 <file_name>`

### Unstaging Files with Git Restore

- `git restore --staged <file_name>` – remove the <file_name> from staging area for the next commit but keep its content in the working directory

### Removing Untracked Files

- `git clean -fdn` – clean all untracked files and return the repository to the state of the last commit (HEAD)
  - `-f` – force
  - `-d` – include untracked directories
  - `-n` – perform a "dry run" and display the files and directories that would be removed
