# Bandit Level 11

## Objective

The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files and directories, including hidden ones.
     ```bash
     ls -l -a
     ```

2. **View File Contents:**
   - Used the `cat` command to view the contents of `data.txt`, which was base64 encoded.
     ```bash
     cat data.txt
     ```

3. **Decode Base64 Data:**
   - Used the `base64` command with the `-d` option to decode the base64 encoded file and retrieve the password.
     ```bash
     base64 -d data.txt
     ```
   - **Explanation:** The `-d` option stands for decode, which converts the base64 encoded data back into its original format.

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cat data.txt`**: Displays the contents of the `data.txt` file.
- **`base64 -d data.txt`**: Decodes the base64 encoded content of the `data.txt` file, revealing the password.

## Password

The password for Level 10 is: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
