# Print Directories in `$PATH`

On Unix-like systems, you can inspect the `PATH` environment variable of your shell to see the list of directories the system will search when looking for executables.

```bash
echo $PATH | tr ':' '\n'
