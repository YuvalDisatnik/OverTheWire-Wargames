# Bandit Level 08

## Objective

The objective of Level 8 is to find the password for the next level, which is stored in the file `data.txt` and is located next to the word "millionth."

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files in the current directory, including hidden files.
     ```bash
     ls -l -a
     ```
   - **Explanation:** This command lists all files and directories, revealing `data.txt`.

2. **View File Contents:**
   - Used the `cat` command to display the contents of `data.txt`.
     ```bash
     cat data.txt
     ```
   - **Explanation:** This command shows the content of the file to understand its structure and look for the required information.

3. **Search for the Word "millionth":**
   - Used the `grep` command to find the line containing the word "millionth."
     ```bash
     grep "millionth" data.txt
     ```
   - **Explanation:** This command searches for the specified word in the file and outputs the line containing it. The password is located next to this word.

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cat data.txt`**: Displays the contents of `data.txt`.
- **`grep "millionth" data.txt`**: Searches for the word "millionth" in `data.txt` and prints the line containing it.

## Password

The password for Level 8 is: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
