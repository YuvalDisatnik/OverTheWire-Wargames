# Bandit Level 15

## Objective

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## Solution

### Steps Taken

1. **Connect Using OpenSSL:**
   - Used the command to connect to the specified port on localhost with SSL.
     ```bash
     openssl s_client -connect localhost:30001
     ```

2. **Submit Previous Password:**
   - Once the connection was established, typed the password for the previous level:
     ```plaintext
     8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
     ```
   - Pressed enter to submit the password.

3. **Retrieve New Password:**
   - As a response, received the password for Level 16:
     ```plaintext
     kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
     ```

### Commands Used

- **`openssl s_client -connect`**: Establishes a secure SSL/TLS connection to a specified host and port.

## Password

The password for Level 15 is: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
