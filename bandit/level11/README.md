# Bandit Level 11

## Objective

The goal of Level 11 is to retrieve the password from the `data.txt` file, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions using the ROT13 cipher.

## Solution

### Steps Taken

1. **List Directory Contents:**
   - Used the `ls` command with `-l` and `-a` options to view all files and directories, including hidden ones.
     ```bash
     ls -l -a
     ```

2. **View File Contents:**
   - Used the `cat` command to display the contents of `data.txt`, which contained ROT13 encoded text.
     ```bash
     cat data.txt
     ```

3. **Understand ROT13 Encoding:**
   - Referenced the ROT13 cipher on Wikipedia, which uses the transformation `tr 'A-Za-z' 'N-ZA-Mn-za-m'` to encode and decode text.
   - The ROT13 encoding rotates each letter by 13 positions in the alphabet.

4. **Decode ROT13 Encoded Text:**
   - Applied the `tr` command to decode the ROT13 text by rotating the characters back to their original form.
     ```bash
     cat data.txt | tr 'N-ZA-Mn-za-m' 'A-Za-z'
     ```

### Commands Used

- **`ls -l -a`**: Lists all files and directories with detailed information, including hidden files.
- **`cat data.txt`**: Displays the contents of the file `data.txt`.
- **`tr 'N-ZA-Mn-za-m' 'A-Za-z'`**: Translates (rotates) characters in the input text from ROT13 encoding to the original alphabet.

## Password

The password for Level 11 is: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
