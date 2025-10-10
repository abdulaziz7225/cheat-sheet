# `grep` Command

The `grep` command searches for patterns in each file's contents. Grep will print each line that matches a pattern we provide

- `grep "chicken" animals.txt` – print each line from the `animals.txt` file that contains the pattern "chicken"
- `grep -i "Chapter" book.txt` – print all matching lines from the `book.txt` file that contain the word "chapter" in any casing (case insensitive)
- `grep -n "chicken" animals.txt` – prefix each line of output with 1-based line number within its input file
- `grep -c PATTERN somefile` – print a count of matching lines for each input file
- `grep -o PATTERN somefile` – print only the matched (non-empty) parts of a matching line rather than the entire line containing each match
- `grep -m NUM PATTERN somefile` – print the first `NUM` times of matching lines

## Word Search

Use the `-w` option to ensure that `grep` only matches words, rather than fragments located inside of other words. A word is defined by non-word characters on either side (start of line, spaces, end of line, punctuation, etc.)

- `grep -w "cat" book.txt` – match the word "cat" but not "catheter"

## Context Line Control

- `grep -A NUM PATTERN somefile` – print `NUM` lines of trailing context after matching lines
- `grep -B NUM PATTERN somefile` – print `NUM` lines of leading context before matching lines
- `grep -C NUM PATTERN somefile` – print `NUM` lines of leading and trailing context for matching lines

## Recursive Search

Use the `-r` option to perform a recursive search which will include all files under a directory, subdirectories and their files, and so on. If we don't specify a starting directory, `grep` will search the current working directory

- `grep -r "chicken ~/Desktop"` – search the "Desktop" folder in home directory and any nested directories for lines that contain "chicken"

## Regular Expression (RegEx)

We can provide regular expressions to `grep`. Regular expressions helps us match complex patterns

- `.` – matches any single character
- `^` – matches the start of a line
- `$` – matches the end of a line
- `[abc]` – matches any character in the set
- `[^abc]` – matches any char NOT in set
- `[A-Z]` – matches characters in a range
- `*` – repeat previous expression 0 or more times
- `\` – escape meta-characters

### Extended Regular Expression

- `grep -E PATTERN somefile` – interpret patterns as extended regular expressions
- `egrep PATTERN somefile` – same as `grep -E PATTERN somefile`

### RegEx Patterns

- `grep -iw "p...." somefile` – match case-insensitive search for words that starts with the letter `p` and has 4 more characters
- `grep -w "^I" somefile` – match all lines that start with the `I` pronoun
- `grep -E "PATTERN$" somefile` – match all lines that end with the `PATTERN`
- `grep -wE "birds?" somefile` – match all lines that have the word "bird" or "birds". The letter before `?` symbol is meant optional during the search
- `grep -E [aeiou]{2} somefile` – match all lines that have two consecutive vowel letters
- `grep -E [aeiou]{3,4} somefile` – match all lines that have three to four consecutive vowel letters
