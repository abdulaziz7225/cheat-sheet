# Shortcuts

- `CTRL + l` – clear the entire screen in terminal (same as typing `clear` command)

## Line Jumping

- `CTRL + a` – move the cursor to the beginning of the line
- `CTRL + e` – move the cursor to the end of the line

## Move Characters

- `CTRL + f` – move the cursor forward one character at a time (same as the `>` right arrow)
- `CTRL + b` – move the cursor backwards one character at a time (same as the `<` left arrow)

## Jump Words

- `ALT + f` – move the cursor forward one word
- `ALT + b` – move the cursor backwards one word

## Swapping

- `CTRL + t` – swap the current character under the cursor with the one preceding it
- `ALT + t` – swap the current word under the cursor with the one preceding it

## Kill the Line

- `CTRL + k` – kill the text from the current cursor location (inclusive) until the end of the line
- `CTRL + u` – kill the text from the beginning of the line to the current cursor location (exclusive)

## Kill a Word

- `ALT + d` – kill the text from the current cursor location (inclusive) through the end of the word
- `CTRL + w` or `ALT + backspace` – kill the text from the beginning of the word to the current cursor location (exclusive)
- `CTRL + d` – delete the character under the cursor, not one before the cursor

## Revive Text (Yanking)

When we kill text using commands like `CTRL + k`, `CTRL + u`, `ALT + d`, `ALT + backspace`, the `killed` text is stored in a memory in an area known as the `kill-ring`

- `CTRL + y` – retrieve the most recently killed text
