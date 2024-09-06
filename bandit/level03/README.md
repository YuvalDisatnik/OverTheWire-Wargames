# Bandit Level 03

## Objective

The objective of Level 3 is to retrieve a password from a hidden file located in the `inhere` directory.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files and directories, including hidden ones.
     ```bash
     ls -l -a
     ```

2. **Navigate to `inhere` Directory:**
   - Used the `cd` command to change into the `inhere` directory.
     ```bash
     cd inhere
     ```

3. **List Directory Contents Again:**
   - Used the `ls` command with `-l` and `-a` options to view the contents of the `inhere` directory.
     ```bash
     ls -l -a
     ```

4. **Read the Hidden File:**
   - Identified the file named `...Hiding-From-You` from the directory listing. Used `cat` to display its contents.
     ```bash
     cat ...Hiding-From-You
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cd inhere`**: Changes the current directory to `inhere`.
- **`cat ...Hiding-From-You`**: Displays the contents of the `...Hiding-From-You` file, which contains the password.

## Password

The password for Level 3 is: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
