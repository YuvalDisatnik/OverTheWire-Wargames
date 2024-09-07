# Bandit Level 12

## Objective

The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed. The task involves decompressing multiple layers to reveal the final password.

## Solution

### Steps Taken

1. **Create a Temporary Directory:**
   - Used `mktemp -d` to create a secure temporary directory for processing.
     ```bash
     mktemp -d
     ```

2. **Copy and Rename File:**
   - Copied the `data.txt` file into the temporary directory.
     ```bash
     cp data.txt /path/to/temp/dir/
     ```
   - Renamed the file for ease of use.
     ```bash
     mv /path/to/temp/dir/data.txt /path/to/temp/dir/data2.txt
     ```

3. **Convert Hexdump to Binary:**
   - Used `xxd -r` to convert the hexdump file back to its binary format.
     ```bash
     xxd -r data2.txt reversed_data
     ```

4. **Decompress Layers:**
   - Identified the file type using `file` and performed the necessary decompression steps.
   
   Each time a new file type was detected, renamed the file with the appropriate extension and decompressed accordingly.
   
   This involved:
     ```bash
     gzip -d compressed_data.gz
     bzip2 -d compressed_data.bz2
     tar -xvf compressed_data.tar
     ```
   - Renamed files with appropriate extensions before each decompression step to handle the file correctly.

5. **Inspect Extracted Files:**
   - After decompression and extraction, located the final ASCII text file that contained the password.

### Commands Used

- **`mktemp -d`**: Creates a secure temporary directory.
- **`cp`**: Copies files.
- **`mv`**: Renames or moves files.
- **`xxd -r`**: Converts a hexdump back to binary.
- **`gzip -d`**: Decompresses gzip files.
- **`bzip2 -d`**: Decompresses bzip2 files.
- **`tar -xvf`**: Extracts files from a tar archive.
- **`file`**: Identifies the type of a file.

## Password

The password for Level 12 is: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
