# Work with Files

## `cat`, `tac`, and `rev` commands

- `cat <filename>` – read the content of a file and print it out
- `cat <file1> <file2>` – concatenate the contents of given files and output the second file immediately after the first one
- `tac <filename>` – concatenate and print files in reverse **"vertically"**. It prints each line of a file, starting with the last line
- `rev <filename>` – print the content of a file, reversing the order of each line. It is a **"horizontal"** reverse whereas `tac` is a **"vertical"** reverse

## `less` command

- `less somefile.txt` – display the content of `somefile.txt`, one page at a time

### `less` navigation

When viewing a file using `less`

- press `space` or `f` to go to the next page
- press `b` to go back to the previous page
- press `Enter` or `↓` (down) to scroll by one line
- type forward slash `/` followed by a pattern to search
- press `q` to quit

## `head` and `tail` commands

- `head filename.txt` – print the first 10 lines of the given file by default
- `head -n 21 filename.txt` – specify the number of lines for `head` to print out
  - `head --lines 21 filename.txt`– the same as above
  - `head -21 filename.txt` – the same as above
- `tail filename.txt` - print the last 10 lines of the given file by default
- `tail -n 13 filename.txt` – specify the number of lines for `tail` to print out
- `tail -f filename.txt` – output appended data as the file grows

## Word Count command

The word count command can tell us the number of words, lines, or bytes in files. By default, it prints out three numbers: the number of lines, words and bytes in a file

- `wc -l somefile.txt` – print the number of lines in the given file
- `wc -w somefile.txt` – print the number of words
- `wc -m somefile.txt` – print the number of characters
- `wc -c somefile.txt` – print the number of bytes (some characters take more than 1 byte in UTF-8 encoding)
