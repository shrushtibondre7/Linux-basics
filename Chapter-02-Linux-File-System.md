# Chapter 2 - Linux File System

# What is the Linux File System?

The Linux File System is a hierarchical structure used to organize and store files and directories. Everything in Linux starts from the root directory (`/`), and all files, folders, and devices are organized under it.

Unlike Windows, Linux does not use drive letters (C:, D:, etc.). Instead, it follows a single directory tree beginning with the root directory.

---

# Linux Directory Structure

```
                    /
                    |
 ------------------------------------------------------------------
 |     |      |      |      |      |      |      |      |         |
bin   boot   dev    etc    home   lib    media   opt    proc     root
 |      |      |      |       |      |       |      |       |        |
sbin   tmp    usr    var    mnt    srv     sys    run
```

---

# Important Linux Directories

## 1. /

The root directory is the top-level directory in Linux. Every other directory exists under it.

Example:

```bash
cd /
```

---

## 2. /home

Contains home directories of normal users.

Example:

```bash
/home/shrushti
/home/ubuntu
```

Command:

```bash
cd /home
```

---

## 3. /root

Home directory of the root (administrator) user.

Command:

```bash
cd /root
```

---

## 4. /bin

Stores essential user commands.

Examples:

- ls
- cp
- mv
- rm
- cat
- pwd

Command:

```bash
ls /bin
```

---

## 5. /sbin

Contains system administration commands.

Examples:

- reboot
- shutdown
- fdisk
- mkfs

Command:

```bash
ls /sbin
```

---

## 6. /etc

Stores configuration files.

Examples:

- passwd
- shadow
- hosts
- fstab

Command:

```bash
ls /etc
```

---

## 7. /var

Contains files that change frequently.

Examples:

- Log files
- Cache
- Mail
- Spool files

Command:

```bash
cd /var/log
```

---

## 8. /tmp

Stores temporary files.

Files inside this directory may be removed automatically after a reboot.

Command:

```bash
cd /tmp
```

---

## 9. /usr

Contains user programs, libraries, and documentation.

Subdirectories:

- /usr/bin
- /usr/lib
- /usr/local

---

## 10. /boot

Contains files required to boot Linux.

Examples:

- Kernel
- GRUB Boot Loader

Command:

```bash
ls /boot
```

---

## 11. /dev

Contains device files.

Examples:

- /dev/sda
- /dev/xvda
- /dev/null

Command:

```bash
ls /dev
```

---

## 12. /proc

Virtual directory containing information about running processes and the kernel.

Command:

```bash
ls /proc
```

---

## 13. /sys

Contains information related to hardware and kernel devices.

---

## 14. /opt

Stores optional third-party software.

Example:

Google Chrome
Visual Studio Code

---

## 15. /media

Automatically mounts removable devices such as USB drives.

---

## 16. /mnt

Used for manually mounting storage devices.

---

## 17. /run

Contains temporary runtime information created after system startup.

---

# Linux File Types

Linux supports different file types.

| Symbol | File Type |
|---------|-----------|
| - | Regular File |
| d | Directory |
| l | Symbolic Link |
| c | Character Device |
| b | Block Device |
| p | Named Pipe |
| s | Socket |

Example:

```bash
ls -l
```

---

# Absolute Path

An absolute path always starts from the root directory (`/`).

Example:

```bash
/home/shrushti/Documents/file.txt
```

---

# Relative Path

A relative path starts from the current working directory.

Example:

```bash
Documents/file.txt
```

---

# Special Path Symbols

| Symbol | Meaning |
|---------|---------|
| . | Current Directory |
| .. | Parent Directory |
| ~ | Home Directory |
| / | Root Directory |

Examples:

```bash
cd .
cd ..
cd ~
cd /
```

---

# Useful Commands

Display Current Directory

```bash
pwd
```

List Files

```bash
ls
```

Long Listing

```bash
ls -l
```

Hidden Files

```bash
ls -la
```

Change Directory

```bash
cd
```

Create Directory

```bash
mkdir project
```

Remove Directory

```bash
rmdir project
```

Create File

```bash
touch notes.txt
```

Display File

```bash
cat notes.txt
```

Copy File

```bash
cp file1 file2
```

Move File

```bash
mv file1 file2
```

Delete File

```bash
rm file.txt
```

---

# Best Practices

- Organize files into meaningful directories.
- Avoid storing important files in `/tmp`.
- Use absolute paths in scripts when possible.
- Regularly clean unnecessary files.
- Protect system directories from accidental modification.

---

# Summary

In this chapter, we learned:

- Linux File System
- Linux Directory Structure
- Important Directories
- Linux File Types
- Absolute and Relative Paths
- Special Path Symbols
- Common File Management Commands

---

# Interview Questions

## 1. What is the root directory in Linux?

The root directory (`/`) is the top-most directory from which all other directories originate.

---

## 2. What is the difference between `/home` and `/root`?

- `/home` stores home directories of normal users.
- `/root` is the home directory of the root (administrator) user.

---

## 3. What is stored in `/etc`?

Configuration files for the operating system and applications.

---

## 4. What is the purpose of `/var`?

It stores variable data such as logs, cache, mail, and spool files.

---

## 5. What is the difference between an absolute path and a relative path?

- An absolute path starts from the root directory (`/`).
- A relative path starts from the current working directory.

---

## Practice Commands

```bash
pwd
ls -l
ls -la
cd /home
cd ..
mkdir demo
cd demo
touch file.txt
cat file.txt
cp file.txt backup.txt
mv backup.txt notes.txt
rm notes.txt
rmdir demo
```
