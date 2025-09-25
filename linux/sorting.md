# Sorting

The sort command outputs the sorted content of a file (it does not change the file itself). By default, it will sort the lines of a file alphabetically

- `sort filename.txt` – print each line of the give file sorted in alphabetical order
- `sort -r filename.txt` – print each line of the give file sorted in **reverse** alphabetical order
- `sort -n filename.txt` – print each line from the given file sorted in numerical order
- `sort -u filename.txt` – ignore duplicates and only sort unique values
- `sort -k2 filename.txt` – sort the given file by a particular **column**, in this case by column 2
