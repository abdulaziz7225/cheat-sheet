# `find` Command

`find` command on its own list every single file and directory nested in the current working directory

- `find friends/` – print all files and directories inside the `friends` directory including nested folders

## Find by Type

We can tell `find` command to only find by file type: only print files, directories, symbolic links, etc using the `-type` option

- `find -type f` – limit the search result to files only
- `find -type d` – limit the search result to directories

## Find by Name

We can provide a specific pattern for `find` to use when matching filenames and directories with the `-name` option. We need to enclose our pattern in quotes

- `find ~/Desktop/ -name "*.txt"` – find all files on the Desktop folder that ends with the `.txt` extension
- `find -iname "*closed*"` – enable case insensitive search to find files or directories that have the word `closed` on their name

## Find by Size

We can use the `-size` option to find files of a specific size

- `find -size +1G` – find all files larger than 1 gigabyte
- `find -size -50M` – find all files under 50 megabytes
- `find -size 20k` – find all files that are exactly 20 kilobytes in size

## Find by Owner

- `find -user <username>` – find files and directories that only belong to a particular user

## Find by Time

### Timestamps

- `mtime` – modification time is when a file was last modified (a.k.a. when its contents last changed)
- `ctime` – change time is when a file was last changed. This occurs anytime `mtime` changes but also when we rename a file, move it, or alter permissions
- `atime` – access time is updated when a file is read by an application or a command like `cat`

### `-mtime` option

- `find -mtime n` – match files and folders that were last modified `24*n` hours ago
- `find -mmin -20` – match files that were modified LESS than 20 minutes ago
- `find -mmin +60` – match files that were modified more than 60 minutes ago

### `-ctime` option

- `find -cmin -20` – match files whose content or metadata were changed LESS than 20 minutes ago
- `find -cmin +60` – match files whose content or metadata were changed more than 60 minutes ago

### `-atime` option

- `find -amin n` – match files that were last accessed `n` minutes. We can specify `+n` _for greater than n minutes ago_ and `-n` _for less than n minutes ago_
- `find -anewer somefile` – match files that have been accessed more recently than the provided file

## Logical Operators

We can also use the `-and`, `-or`, and `-not` (same as `!`) operators to create more complex queries

- `find -name "*chick*" -or -name "*kitty*"` – match all files and folders that have either the word `chick` or `kitty` on their names
- `find -type f -not -name "*.html"` – match all files that do not end with the `.html` extension
- `find -type f ! -name "*.html"` – same as `find -type f -not -name "*.html"`

## User-defined Actions

We can provide `find` with our own action to perform using each matching path name. The syntax is `find -exec command '{}' ';'` The `{}` are a placeholder for the current path name (for each match), and the semicolon is required to indicate the end of the command

- `find -name "*broken*" -exec rm '{}' ';'` – delete every file and folders that contain the word `broken` in their names. Note that we need to wrap the `{}` and `;` in quotes because those characters have special meanings otherwise
- `find -name "*broken*" -ok rm '{}' ';'` – ask to execute the given command for each match instead of executing it for all file
- `find -type f -user optimus -exec ls -l '{}' ';'` – find all files that are owned by the user `optimus` and then list out the full details for each match using `ls -l`
- `find -type f -name "*.html" -exec cp '{}' '{}_COPY' ';'` – find all files that end with `.html` and create a copy of each one using `cp` command

### `xargs` Command

When we provide a command for `find` via `-exec` option, that command is executed separately for every single element. We can instead use a special command called `xargs` to build up the input into a bundle that will be provided as an argument list to the next command

- `find -name "*.txt" | xargs ls -l` – same as `find -name "*.txt" -exec ls -l '{}' ';'`
- `find -name "chapter[1-4].txt" | xargs cat > full_book.txt` – find four individual chapter files (chapter1, chapter2, chapter3, and chapter4) and pass them to the `cat`, which then outputs
the combined contents to a file called `full_book.txt`
- `echo "hello" "world" | xargs mkdir` – `xargs` command accepts the standard output coming from `echo` command and passes them as arguments to `mkdir`
