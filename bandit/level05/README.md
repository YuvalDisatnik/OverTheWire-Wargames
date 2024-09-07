# Bandit Level 06

## Objective

The objective of Level 6 is to retrieve a password from a file located somewhere under the `inhere` directory that satisfies all of the following criteria:
- Human-readable
- Exactly 1033 bytes in size
- Not executable

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
   - Used the `ls` command with `-l` and `-a` options to view the contents of the `inhere` directory, which contained a large number of files.
     ```bash
     ls -l -a
     ```

4. **Filter by File Types:**
   - Used the `find` command combined with `file` to determine the type of each file in the directory.
     ```bash
     find . -type f -exec file {} \;
     ```
   - **Explanation:** This command lists all files and their types, helping to identify human-readable files.

5. **Filter by File Size:**
   - Used `find` to locate files that are exactly 1033 bytes in size.
     ```bash
     find . -type f -size 1033c -exec file {} \;
     ```
   - **Explanation:** The `-size 1033c` option specifies files that are exactly 1033 bytes. This narrowed down the results to files matching the size criterion.

6. **Ensure Files are Not Executable:**
   - Refined the search to find files that are exactly 1033 bytes in size and not executable.
     ```bash
     find . -type f -size 1033c ! -executable -exec file {} \;
     ```
   - **Explanation:** The `! -executable` option excludes files that are executable, ensuring the remaining files meet all criteria.

7. **Retrieve the Password:**
   - Found the file `./maybehere07/.file2` that matched all criteria and used `cat` to read its contents.
     ```bash
     cat ./maybehere07/.file2
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cd inhere`**: Changes the current directory to `inhere`.
- **`find . -type f -exec file {} \;`**: Finds all files and displays their types.
- **`find . -type f -size 1033c -exec file {} \;`**: Finds files that are exactly 1033 bytes in size and displays their types.
- **`find . -type f -size 1033c ! -executable -exec file {} \;`**: Finds files that are exactly 1033 bytes in size and not executable, displaying their types.
- **`cat ./maybehere07/.file2`**: Displays the contents of the file, which contains the password.

## Password

The password for Level 6 is: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
