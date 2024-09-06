# Bandit Level 01

## Objective

The objective of Level 2 is to retrieve a password from a file named `-` in the current directory.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files and directories, including hidden ones.
     ```bash
     ls -l -a
     ```

2. **Read the File:**
   - Identified the `-` file from the directory listing. Because `-` is often used to indicate standard input or output in commands, used `./-` to specify the file explicitly and `cat` to display its contents.
     ```bash
     cat ./-
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information.
- **`cat ./-`**: Displays the contents of the `-` file, using the full path to avoid confusion with command arguments.

## Password

The password for Level 2 is: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
