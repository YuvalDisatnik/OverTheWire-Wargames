# Bandit Level 07

## Objective

The objective of Level 7 is to retrieve a password from a file located somewhere on the server that satisfies all of the following criteria:
- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

## Solution

### Steps Taken

1. **Search for Files by Size:**
   - Used the `find` command to search the entire server (`/`) for files that are exactly 33 bytes in size.
     ```bash
     find / -type f -size 33c
     ```
   - **Explanation:** The `-type f` option searches for files, and `-size 33c` specifies files that are exactly 33 bytes. This command returned many results, including "Permission denied" errors.

2. **Filter by User and Group:**
   - Refined the search to include only files owned by `bandit7` and the group `bandit6`.
     ```bash
     find / -type f -size 33c -user bandit7 -group bandit6
     ```
   - **Explanation:** The `-user bandit7` and `-group bandit6` options filter files by owner and group. The output still included many permission errors.

3. **Suppress Permission Denied Errors:**
   - Redirected error messages to standard output and filtered them out using `grep` to clean the output.
     ```bash
     find / -type f -size 33c -user bandit7 -group bandit6 2>&1 | grep -v "Permission denied"
     ```
   - **Explanation:** `2>&1` redirects the standard error (stderr) to standard output (stdout), and `grep -v "Permission denied"` removes lines containing "Permission denied," making it easier to see the relevant files.

4. **Retrieve the Password:**
   - Located the file `/var/lib/dpkg/info/bandit7.password` that matched all criteria and displayed its contents to retrieve the password.
     ```bash
     cat /var/lib/dpkg/info/bandit7.password
     ```

### Commands Used

- **`find / -type f -size 33c`**: Searches the entire server for files that are exactly 33 bytes in size.
- **`find / -type f -size 33c -user bandit7 -group bandit6`**: Refines the search to include only files owned by `bandit7` and the group `bandit6`.
- **`find / -type f -size 33c -user bandit7 -group bandit6 2>&1 | grep -v "Permission denied"`**: Suppresses permission errors and filters them out, displaying only relevant files.
- **`cat /var/lib/dpkg/info/bandit7.password`**: Displays the contents of the file containing the password.

## Password

The password for Level 7 is: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
