# `chmod` Command

We can use the `chmod` command (change mode) to change the permissions or mode bits of a file or directory

## Permissions

| Character | Effect On Files                                                                             | Effect On Directories                                                                                                          |
| --------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **r**     | file can be read                                                                            | directory's contents can be listed                                                                                             |
| **w**     | file can be modified                                                                        | directory's contents can be modified (create new files, rename files/folders) but only if the executable attribute is also set |
| **x**     | file can be treated as a program to be executed                                             | allow a directory to be entered or `cd`ed into                                                                                 |
| **-**     | file cannot be read, modified, or executed depending on the location of the **-** character | directory contents cannot be shown, modified, or `cd`ed into depending on the location of the **-** character                  |

## Use `chmod` to alter permissions

- **Who** we are changing permissions for
- **What** change are we making? Adding? Removing?
- **Which** permissions are we setting?

### Who

- `u` – user (the owner of the file)
- `g` – group (members of the group the file belongs to)
- `o` – others (the "world")
- `a` – all of the above

### What

- `-` – remove the permission
- `+` – grant the permission
- `=` – set a permission and remove others

### Which

- `r` – read permission
- `w` – write permission
- `x` – execute permission
