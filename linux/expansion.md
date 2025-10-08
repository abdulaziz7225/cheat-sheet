# Expansion and Substitution

## Wildcard Characters

### Asterisk `*` Character

The asterisk `*` character represents zero or more characters in a filename

- `ls *.html`– match any files that end with `.html` like `index.html` and `navbar.html`
- `cat blue*` – match any files that start with **blue** like `blue.html` or `bluesteel.js`

### Question Mark `?` Character

The question mark `?` character represents any single character

- `ls app.??` – match any files named `app` that end with two character file extensions like `app.js` or `app.py`, but NOT `app.css`
- `ls pic?.png` – match `pic1.png`, `pic2.png`, `pic3.png`, but also `picA.png` or `picx.png`

### Range Wildcards

Inside of square brackets `[]` we can specify a range of characters to match

- `ls pic[123].png` – only match `pic1.png`, `pic2.png`, and `pic3.png`
- `ls file[0-9]` – match `file1`, `file2`, `file3`, up to `file9`
- `ls [A-F]*` – match any files that begin with a capital A, B, C, D, E, or F

### Negating Ranges

Inside of square brackets `[]` we can specify a range of characters to NOT match, using a caret `^`

- `ls [^a]*` – match any files that do NOT start with `a`
- `ls [^0-9]*` – match any files that do NOT start with a numeric digit `(0-9)`

### Character Classes

Predefined named characters to use for range and negating wildcards

- `[:alpha:]` – alphabetic characters, upper and lower
- `[:digit:]` – digits 0-9
- `[:lower:]` – lower case letters
- `[:upper:]` – upper case letters
- `[:blank:]` – blank characters: space and tab
- `[:punct:]` – punctuation characters
- `[:alnum:]` – alphanumeric characters (alpha + digit)

## Brace Expansion

Brace expansion is used to generate arbitrary strings. Basically, it will generate multiple strings based on a pattern. We provide a set of strings inside of curly braces `{}`, as well as optional surrounding prefixes and suffixes

- `touch page{1,2,3}.txt` – generate three new files: `page1.txt`, `page2.txt`, and `page3.txt`
- `mkdir jan{1..31}` – generate a sequence of the provided numeric range and create folders `jan1`, `jan2`, `jan3`, etc until `jan31`
- `echo {2..10..2}` – define the interval range with a third value. This prints out the numbers 2, 4, 6, 8, and 10
- `touch group-{a..e}.txt` – specify alphabetical ranges. This example generates the files `group-a.txt`, `group-b.txt`, `group-c.txt`, `group-d.txt`, and `group-e.txt`

### Multiple brace expansions

- `echo {a,b,c}{1,2,3}` – print out `a1 a2 a3 b1 b2 b3 c1 c2 c3`
- `echo {b,r}{eef,at,ag}` – print out `beef bat bag reef rat rag`
- `echo {x,y{1..5},z}` – print out `x y1 y2 y3 y4 y5 z`

## Arithmetic Expression

The shell performs arithmetic expression via expansion using the `$((expression))` syntax. Inside the parentheses, we can
write arithmetic expressions using:

- `+` addition
- `-` subtraction
- `*` multiplication
- `/` division
- `**` exponentiation
- `%` modulo (remainder operator)

## Command Substitution

We can use the `$(command)` or `` `command` `` syntax (backtick) to display the output of another command

- `echo "today is $(date)"` – print out `today is Wed Oct  8 23:09:35 CEST 2025`
- `` echo "today is `date`" `` – print out the same output as above

## Quoting

### Double Quotes

If we wrap text in double quotes, the shell will respect our spacing and will ignore special characters except for dollar sign `$`, backslash `\`, and backtick `` ` ``

### Single Quotes

Use single quotes to suppress all forms of substitution

- `echo "$((2+2)) is 4"` – print out `4 is 4`
- `echo '$((2+2)) is 4'` – print out `$((2+2)) is 4`

### Escaping

To selectively prevent expansion or substitution for specific characters, we can prefix them with a single backslash `\`

- `echo "$5.00"` – print out `.00`
- `echo "\$5.00"` – print out `$5.00`
