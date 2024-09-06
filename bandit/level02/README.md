# Bandit Level 02

## Objective

The objective of Level 2 is to retrieve a password from a file named `spaces in this filename` in the current directory.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files and directories, including hidden ones.
     ```bash
     ls -l -a
     ```

2. **Read the File:**
   - Identified the file named `spaces in this filename`. Used `cat` to display its contents. 
   - **Method 1:** Escaped spaces in the file name with backslashes.
     ```bash
     cat spaces\ in\ this\ filename
     ```
   - **Method 2:** Used quotes around the file name to handle spaces.
     ```bash
     cat "spaces in this filename"
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information.
- **`cat spaces\ in\ this\ filename`**: Displays the contents of the file, using backslashes to escape spaces.
- **`cat "spaces in this filename"`**: Displays the contents of the file, using quotes to handle spaces in the file name.

## Password

The password for Level 2 is: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
