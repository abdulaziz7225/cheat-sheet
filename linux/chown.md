# `chown` Command

The `chown` command is used to change the owner and/or the group owner of a specific file or directory

- `chown USER[:GROUP] FILE(s)` – change the owner and group owner of a file or multiple files
- `chown optimus somefile.txt` – make _optimus_ the owner of the given file
- `chown :animals horses.txt` – change the group owner of _horses.txt_ to the group named _animals_
- `chown optimus:cities capitals.txt` – change the owner of the _capitals.txt_ file to _optimus_ and the group owner to _cities_

## Groups

- `groups USERNAME` – view the groups that a given user belongs to
- `groups` – the command defaults to the current user in case _USERNAME_ isn't provided
- `sudo addgroup GROUP` – create a new group
- `sudo adduser USER GROUP` – add a user to a group
- `sudo groupdel GROUP` – delete a group
