# Linux File Permissions

## Permission Types

- r (read) - Permission to read a file
- w (write) - Permission to modify a file
- x (execute) - Permission to execute a file

## Permission Commands

- chmod - Change file permissions
- chown - Change file owner

## Numeric Permissions

- 755 - Owner: rwx, Group: r-x, Others: r-x
- 644 - Owner: rw-, Group: r--, Others: r--

## Examples

- chmod 755 script.sh
- chmod 644 file.txt
- chown user:group file.txt
