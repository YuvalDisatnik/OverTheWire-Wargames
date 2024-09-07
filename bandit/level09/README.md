# Bandit Level 10

## Objective

The password for the next level is stored in the file `data.txt` and is the only line of text that contains a readable string starting with `==`.

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

3. **Extract Readable Strings:**
   - Used the `strings` command to extract readable strings from `data.txt`. This command displays sequences of printable characters from the file.
     ```bash
     strings data.txt
     ```

4. **Filter Specific Lines:**
   - Used `grep` to filter the strings that start with `==`, as instructed.
     ```bash
     strings data.txt | grep "=="
     ```
   - **Explanation:** 
     - `strings data.txt` extracts readable strings from `data.txt`.
     - `grep "=="` filters these strings to show only those starting with `==`. The password was identified from the output.

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cat data.txt`**: Displays the contents of the `data.txt` file.
- **`strings data.txt`**: Extracts and displays readable strings from the `data.txt` file.
- **`strings data.txt | grep "=="`**: Filters the output of `strings` to show only lines that start with `==`.

## Password

The password for Level 10 is: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
