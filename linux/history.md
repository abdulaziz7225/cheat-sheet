# History

Bash keeps a record of previously entered commands. This record is stored in the `~/.bash_history` file. We can scroll through past commands one at a time using the `↑` (up) and `↓` (down) arrow keys.

- `history` – view the entire command history
- `history | less` – view the full history with `less` for easier navigation, similar to a `man` page
- `echo $HISTFILESIZE` – show the maximum number of lines the `~/.bash_history` file can store
- `echo $HISTSIZE` – show the maximum number of lines displayed in the terminal when you run the `history` command

## History Expansion

We can easily re-run an earlier command if we have its line number from the history like `!somenumber`:

- `!73` – run the 73rd command in the history list

## Search History

- `CTRL + r` – enter **reverse-i-search** mode. As you type, Bash searches your command history and displays the best match. Press `CTRL + r` repeatedly to cycle through additional matches
