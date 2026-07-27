# Chapter 3 - Linux Basic Commands

# Introduction

Linux commands are instructions entered in the terminal to interact with the operating system. They help users perform tasks such as managing files, directories, users, processes, networking, and system resources.

Understanding Linux commands is one of the most important skills for Cloud and DevOps Engineers.

---

# Command Syntax

```bash
command [options] [arguments]
```

Example:

```bash
ls -l /home
```

- **ls** → Command
- **-l** → Option
- **/home** → Argument

---

# System Information Commands

## 1. whoami

Displays the currently logged-in user.

```bash
whoami
```

Example Output

```
ubuntu
```

---

## 2. hostname

Displays the hostname of the system.

```bash
hostname
```

---

## 3. hostnamectl

Displays detailed hostname and operating system information.

```bash
hostnamectl
```

---

## 4. pwd

Displays the current working directory.

```bash
pwd
```

Example Output

```
/home/ubuntu
```

---

## 5. uname

Displays Linux kernel information.

```bash
uname
```

Display all information.

```bash
uname -a
```

---

## 6. cat /etc/os-release

Displays Linux distribution details.

```bash
cat /etc/os-release
```

---

## 7. date

Displays current date and time.

```bash
date
```

---

## 8. cal

Displays the calendar.

```bash
cal
```

---

## 9. history

Displays previously executed commands.

```bash
history
```

---

# File & Directory Commands

## 1. ls

Lists files and directories.

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

---

## 2. cd

Changes the current directory.

```bash
cd Documents
```

Go back one directory

```bash
cd ..
```

Go to Home Directory

```bash
cd ~
```

Go to Root Directory

```bash
cd /
```

---

## 3. mkdir

Creates a new directory.

```bash
mkdir DevOps
```

Create multiple directories

```bash
mkdir aws docker kubernetes
```

---

## 4. rmdir

Deletes an empty directory.

```bash
rmdir DevOps
```

---

## 5. touch

Creates an empty file.

```bash
touch notes.txt
```

---

## 6. cat

Displays file contents.

```bash
cat notes.txt
```

Create a file

```bash
cat > notes.txt
```

---

## 7. cp

Copies files or directories.

```bash
cp file1.txt file2.txt
```

Copy directory

```bash
cp -r project backup
```

---

## 8. mv

Moves or renames files.

Rename file

```bash
mv old.txt new.txt
```

Move file

```bash
mv notes.txt /home/ubuntu
```

---

## 9. rm

Deletes files.

```bash
rm notes.txt
```

Delete directory recursively

```bash
rm -r project
```

Force delete

```bash
rm -rf project
```

⚠️ Be careful while using `rm -rf` because deleted files cannot be recovered easily.

---

# Search Commands

## find

Searches files and directories.

```bash
find /home -name notes.txt
```

Find only directories

```bash
find /home -type d
```

Find only files

```bash
find /home -type f
```

---

## grep

Searches text inside files.

```bash
grep ubuntu file.txt
```

Ignore case

```bash
grep -i ubuntu file.txt
```

---

# File Viewing Commands

## head

Displays first 10 lines.

```bash
head file.txt
```

---

## tail

Displays last 10 lines.

```bash
tail file.txt
```

Live log monitoring

```bash
tail -f /var/log/syslog
```

---

## less

Displays large files page by page.

```bash
less file.txt
```

---

# Disk & Memory Commands

## df -h

Displays disk usage.

```bash
df -h
```

---

## du -sh

Displays directory size.

```bash
du -sh Documents
```

---

## free -h

Displays memory usage.

```bash
free -h
```

---

## lsblk

Displays block devices.

```bash
lsblk
```

---

# CPU Information

```bash
lscpu
```

Displays processor details.

---

# Network Commands

## ping

Checks network connectivity.

```bash
ping google.com
```

---

## ip addr

Displays IP address.

```bash
ip addr
```

---

## curl

Retrieves data from a URL.

```bash
curl https://google.com
```

---

## wget

Downloads files.

```bash
wget https://example.com/file.zip
```

---

# Clear Screen

```bash
clear
```

Shortcut

```
Ctrl + L
```

---

# Exit Terminal

```bash
exit
```

---

# Summary Table

| Command | Description |
|----------|-------------|
| pwd | Print current directory |
| ls | List files |
| cd | Change directory |
| mkdir | Create directory |
| rmdir | Remove empty directory |
| touch | Create file |
| cp | Copy files |
| mv | Move or rename files |
| rm | Delete files |
| cat | Display file contents |
| head | First 10 lines |
| tail | Last 10 lines |
| grep | Search text |
| find | Search files |
| df -h | Disk usage |
| free -h | Memory usage |
| lsblk | Block devices |
| history | Command history |
| hostname | Display hostname |
| whoami | Current user |

---

# Interview Questions

### 1. What is the difference between `cp` and `mv`?

- `cp` creates a copy of a file or directory.
- `mv` moves or renames a file or directory.

---

### 2. What is the purpose of the `pwd` command?

It displays the current working directory.

---

### 3. What is the difference between `ls` and `ls -la`?

- `ls` lists visible files and directories.
- `ls -la` lists all files, including hidden files, in long format.

---

### 4. Which command is used to find files?

```bash
find
```

---

### 5. Which command displays memory usage?

```bash
free -h
```

---

# Practice Commands

```bash
pwd
ls -la
mkdir DevOps
cd DevOps
touch notes.txt
cat notes.txt
cp notes.txt backup.txt
mv backup.txt final.txt
find . -name "*.txt"
grep DevOps notes.txt
df -h
free -h
history
```

---

# Conclusion

Linux commands are the foundation of system administration. Mastering these commands improves productivity, troubleshooting, and automation skills, making them essential for Cloud and DevOps Engineers.
