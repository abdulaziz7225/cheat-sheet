# Git Hash-Object

The `git hash-object` command takes some data, stores in `.git/objects` directory and gives us back the unique SHA-1 hash that refers to that data object. In the simplest form, Git simply takes some content and returns the unique key that WOULD be used to store our object. But it does not actually store anything.

- `git hash-object <file_name>` – return unique key that would be used to store the content of the file
- `git hash-object <file_name> -w` – rather than simply outputting the key that git would store in the `objects` folder
- `echo "message" | git hash-object --stdin` – The `--stdin` option tells `git hash-object` to use the content from stdin rather than a file.
- `echo "message" | git hash-object --stdin -w` – rather than simply outputting the key that git would store in the `objects` folder

## Git Cat-File

- `git cat-file -p <object_hash>` – retrieve the data stored in the Git object database. `-p` option tells Git to pretty print the contents of the object based on its type.
- `git cat-file -t <object_hash>` – return the type of object whether it is `tree`, `blob` (binary large object), `commit` or `annotated tag`
- `git cat-file -p main^{tree}` – print the tree object that is pointed to by the tip of `main` branch
