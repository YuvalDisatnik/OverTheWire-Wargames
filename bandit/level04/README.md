# Bandit Level 05

## Objective

The objective of Level 5 is to retrieve a password from the only human-readable file in the `inhere` directory.

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

4. **Identify File Types:**
   - Used the `find` command combined with `file` to determine the type of each file in the directory. This helped to identify which file was human-readable.
     ```bash
     find . -type f -exec file {} \;
     ```
   - **Explanation:** The `find . -type f -exec file {} \;` command finds all files (`-type f`) in the current directory and its subdirectories. For each file found, it executes the `file` command, which outputs the file type. This helps in identifying which files are human-readable, especially when there are multiple files.

5. **Read the Human-Readable File:**
   - Identified that `-file07` was of type `ASCII text`, making it the only human-readable file in the directory.
   - Used `cat` to display the contents of `-file07`, which contained the password.
     ```bash
     cat ./-file07
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cd inhere`**: Changes the current directory to `inhere`.
- **`find . -type f -exec file {} \;`**: Finds all files in the current directory and its subdirectories, and displays their types using the `file` command.
- **`cat ./-file07`**: Displays the contents of the `-file07` file, which contains the password.

## Password

The password for Level 5 is: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
