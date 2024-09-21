# Bandit Level 13

## Objective

The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by the user `bandit14`. For this level, a private SSH key is provided to log in as `bandit14` on localhost using a non-standard SSH port.

## Solution

### Steps Taken

1. **List Files:**
   - Used `ls -l -a` to search for the private SSH key. Found a file named `sshkey.private`.
     ```bash
     ls -l -a
     ```

2. **Inspect the SSH Key:**
   - Used `cat sshkey.private` to view the private key for logging into the next level.
     ```bash
     cat sshkey.private
     ```

3. **SSH into Bandit14:**
   - Used the `ssh` command with the `-i` flag to specify the private key and `-p` to specify port 2220 for the connection to `bandit14@localhost`.
     ```bash
     ssh -i ./sshkey.private -p 2220 bandit14@localhost
     ```

4. **Retrieve the Password:**
   - Once logged in as `bandit14`, used `cat` to display the password stored in `/etc/bandit_pass/bandit14`.
     ```bash
     cat /etc/bandit_pass/bandit14
     ```

### Commands Used

- **`ls -l -a`**: Lists all files, including hidden files, in long format.
- **`cat`**: Displays the contents of files.
- **`ssh -i`**: Specifies the SSH private key to use for logging in.
- **`cat /etc/bandit_pass/bandit14`**: Reads the password file for the next level.

## Password

The password for Level 14 is: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
