# Bandit Level 14

## Objective

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Solution

### Steps Taken

1. **Connect to Specified Port:**
   - Used `nc` to connect to port 30000 on localhost.
     ```bash
     nc localhost 30000
     ```

2. **Submit Previous Level's Password:**
   - Once connected, entered the password for the previous level:
     ```bash
     MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
     ```

3. **Receive the Next Password:**
   - The response provided the password for Level 15:
     ```bash
     8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
     ```

### Commands Used

- **`nc localhost 30000`**: Connects to the specified port (30000) on the local machine.

## Password

The password for Level 15 is: `8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo`
