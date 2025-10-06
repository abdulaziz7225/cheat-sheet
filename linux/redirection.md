# Redirection

Redirection describes the way we can alter the source of standard input, and the destinations for standard output and standard error.

## Standard Output

- `command 1> filename` – redirect the output of a command and overwrite any existing content in the file
- `command > filename` – same as `command 1> filename`, `1` is the default file descriptor of standard output
- `command 1>> filename` – redirect the output of a command and append new content to the end of the file
- `command >> filename` – same as `command 1>> filename`

## Standard Input

- `command 0< filename` – redirect the content of a file to standard input
- `command < filename` – same as `command 0< filename`, `0` is the default file descriptor of standard input

## Standard Error

- `command 2> filename` – redirect the output of any error message and overwrite any existing content in the file
- `command 2>> filename` – redirect the output of any error message and append the error message to the end of the file

## All Together Combined

When redirecting both standard output and standard error, make sure standard output comes **first**. Always redirect standard error after standard output.

- `cat bees.txt ants.txt 1> insects.txt 2> error.txt`

## Short Form

If we want to redirect both standard output and standard error to the same file, we can do it like this:

### Overwrite

- `ls docs 1> output.txt 2> output.txt` – overwrite the content of `docs` folder and any error message to the same file
- `ls docs 1> output.txt 2>&1` – same as `ls docs 1> output.txt 2> output.txt`
- `ls docs &> output.txt` – same as `ls docs 1> output.txt 2> output.txt`

### Append

- `ls docs 1>> output.txt 2>> output.txt` – append the content of `docs` folder and any error message to the end of the same file
- `ls docs 1>> output.txt 2>&1` – same as `ls docs 1>> output.txt 2>> output.txt`
- `ls docs &>> output.txt` – same as `ls docs 1>> output.txt 2>> output.txt`
