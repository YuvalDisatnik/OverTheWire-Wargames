# Bandit Level 09

## Objective

The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to search for the `data.txt` file.
     ```bash
     ls -l -a
     ```

2. **View File Contents:**
   - Used the `cat` command to display the contents of `data.txt`.
     ```bash
     cat data.txt
     ```

3. **Find the Unique Line:**
   - Used a combination of `sort`, `uniq -c`, and `grep` to find the line that occurs only once.
     ```bash
     sort data.txt | uniq -c | grep "1 "
     ```
   - **Explanation:** 
     - `sort data.txt` sorts the lines in `data.txt`.
     - `uniq -c` counts the occurrences of each line in the sorted output.
     - `grep "1 "` filters the output to show only lines that occur exactly once. The password is next to the count `1`.

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cat data.txt`**: Displays the contents of the `data.txt` file.
- **`sort data.txt | uniq -c | grep "1 "`**: Finds lines that occur only once in `data.txt`. The `sort` command arranges lines, `uniq -c` counts them, and `grep "1 "` filters for lines with a count of `1`.

## Password

The password for Level 9 is: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
