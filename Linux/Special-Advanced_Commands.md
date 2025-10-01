# 🔒 Special Permissions in Linux

Linux provides **special permissions** to control how files and directories are accessed beyond normal read/write/execute permissions. These are **SUID, SGID, and Sticky Bit**.

---

## 1️⃣ SUID (Set User ID)

- **Definition:** When **SUID** is set on an executable file, it runs with the **permissions of the file owner**, not the user executing it.
- **Common Use:** `passwd` command runs as root even for normal users.


### Commands:
```bash
# Set SUID on a file
sudo chmod u+s filename

# Check SUID
ls -l filename
# Example output: -rwsr-xr-x 1 root root 12345 Sep 30 12:00 filename

# Remove SUID
sudo chmod u-s filename
```

## 2️⃣ SGID (Set Group ID)

-Definition:
--On files: runs with the group permissions of the file.
--On directories: all new files created inside inherit the directory’s group.
-Use Case: Shared project directories where files automatically belong to the same group.


### Commands:
```bash
# Set SGID on file or directory
sudo chmod g+s filename_or_directory

# Check SGID
ls -l filename_or_directory
# Example for directory: drwxr-sr-x 2 devuser devops 4096 Sep 30 12:10 folder

# Remove SGID
sudo chmod g-s filename_or_directory
```

## 3️⃣ Sticky Bit

-Definition: Mainly used on directories. Prevents users from deleting/renaming files they don’t own, even if they have write permission to the directory.
-Common Use: /tmp directory.


### Commands:
```bash
# Set Sticky Bit on a directory
sudo chmod +t directory_name

# Check Sticky Bit
ls -ld directory_name
# Example output: drwxrwxrwt  7 root root 4096 Sep 30 12:15 tmp

# Remove Sticky Bit
sudo chmod -t directory_name
```
