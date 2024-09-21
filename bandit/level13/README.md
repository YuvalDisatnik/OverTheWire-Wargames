# Bandit Level 13

## Objective

The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user `bandit14`. Instead of directly providing the password, you are given a private SSH key to log into the `bandit14` user account. 

## Solution

### Steps Taken

1. **List Files:**
   - First, I listed all the files in the current directory to locate the SSH private key.
     ```bash
     ls -l -a
     ```
   - The output revealed a file named `sshkey.private`, which is the private SSH key required to log in to the `bandit14` user account.

2. **Inspect the SSH Key:**
   - I viewed the contents of the private SSH key to ensure it was a valid key.
     ```bash
     cat sshkey.private
     ```

3. **SSH into Bandit14:**
   - Using the private key and specifying the correct SSH port (`2220`), I logged into the `bandit14` user account:
     ```bash
     ssh -i ./sshkey.private -p 2220 bandit14@localhost
     ```

4. **Verify Successful Login:**
   - After successfully logging in, I confirmed that I had access to the `bandit14` account, and I could proceed to the next level.

### Commands Used

- **`ls -l -a`**: Lists all files in the current directory, including hidden ones.
- **`cat sshkey.private`**: Displays the contents of the private SSH key.
- **`ssh -i ./sshkey.private -p 2220 bandit14@localhost`**: Logs into the `bandit14` user account using the private key over SSH on port 2220.

## Password

The password for Level 14 is stored in `/etc/bandit_pass/bandit14`, accessible after logging in as `bandit14`.
