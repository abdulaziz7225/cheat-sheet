# `sudo` Command

`sudo`  allows  a permitted user to execute a command as the superuser or another user

- `sudo -l` – see the permitted commands for
the current user
- `su --login USERNAME` – start a shell as another user from within our own shell session
  - `--login` option changes the current directory to home directory of the other user
- `su - USERNAME` – same as `su --login USERNAME`
