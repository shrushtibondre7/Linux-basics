# Chapter 5 - File Permissions

# Introduction

Linux is a secure operating system that controls access to files and directories using permissions.

Permissions determine who can read, write, or execute a file or directory.

Every file and directory has an owner, a group, and permissions.

---

# Why File Permissions are Important?

- Protect sensitive data
- Prevent unauthorized access
- Improve system security
- Allow controlled sharing of files
- Protect system files from accidental deletion

---

# Understanding Linux File Permissions

Run the following command:

```bash
ls -l
```

Example Output

```text
-rwxr-xr-- 1 ubuntu developers 2048 Jul 25 notes.txt
```

Breakdown

```text
-rwxr-xr--
││ │ │
││ │ └── Others
││ └──── Group
│└────── Owner
└──────── File Type
```

---

# File Types

| Symbol | Meaning |
|---------|---------|
| - | Regular File |
| d | Directory |
| l | Symbolic Link |
| c | Character Device |
| b | Block Device |
| p | Named Pipe |
| s | Socket |

---

# Permission Types

| Symbol | Permission | Description |
|---------|------------|-------------|
| r | Read | View file contents |
| w | Write | Modify file |
| x | Execute | Run file or access directory |

---

# Permission Values

| Permission | Value |
|------------|-------|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

---

# Numeric Permission Examples

## 777

Owner → rwx

Group → rwx

Others → rwx

Everyone has full permissions.

⚠ Never use in production.

---

## 755

Owner → rwx

Group → r-x

Others → r-x

Most commonly used for directories.

---

## 700

Owner → rwx

Group → ---

Others → ---

Only owner has access.

---

## 644

Owner → rw-

Group → r--

Others → r--

Commonly used for files.

---

## 600

Owner → rw-

Group → ---

Others → ---

Suitable for private files.

---

# Permission Table

| Number | Binary | Permission |
|---------|---------|------------|
| 0 | --- | No Permission |
| 1 | --x | Execute |
| 2 | -w- | Write |
| 3 | -wx | Write + Execute |
| 4 | r-- | Read |
| 5 | r-x | Read + Execute |
| 6 | rw- | Read + Write |
| 7 | rwx | Read + Write + Execute |

---

# chmod Command

Used to change file permissions.

Syntax

```bash
chmod permission filename
```

Example

```bash
chmod 755 script.sh
```

```bash
chmod 644 notes.txt
```

---

# Symbolic Method

Add execute permission

```bash
chmod +x script.sh
```

Remove write permission

```bash
chmod -w file.txt
```

Give read permission

```bash
chmod u+r file.txt
```

Give execute permission to group

```bash
chmod g+x script.sh
```

Remove permission from others

```bash
chmod o-r file.txt
```

---

# chown Command

Changes file owner.

Example

```bash
sudo chown ubuntu notes.txt
```

Change owner and group

```bash
sudo chown ubuntu:developers notes.txt
```

---

# chgrp Command

Changes group ownership.

Example

```bash
sudo chgrp developers notes.txt
```

---

# umask Command

Displays default permissions.

```bash
umask
```

Example Output

```text
0002
```

Default Permission

File

```text
666 - umask
```

Directory

```text
777 - umask
```

---

# Special Permissions

## SUID

Runs a program with owner's permissions.

Example

```bash
chmod u+s filename
```

---

## SGID

Runs with group's permissions.

```bash
chmod g+s directory
```

---

## Sticky Bit

Only file owner can delete files.

Commonly used on

```text
/tmp
```

Set Sticky Bit

```bash
chmod +t directory
```

---

# View Permissions

```bash
ls -l
```

---

# Check Current User

```bash
whoami
```

---

# Check Owner

```bash
ls -l file.txt
```

---

# Best Practices

- Follow the Principle of Least Privilege.
- Avoid using 777.
- Use 644 for normal files.
- Use 755 for directories.
- Protect sensitive files with 600.
- Review permissions regularly.

---

# Summary

In this chapter, we learned:

- Linux File Permissions
- Owner, Group, Others
- Numeric Permissions
- Symbolic Permissions
- chmod
- chown
- chgrp
- umask
- SUID
- SGID
- Sticky Bit

---

# Interview Questions

## 1. What are Linux file permissions?

They define who can read, write, and execute a file or directory.

---

## 2. What does 755 mean?

Owner → Read, Write, Execute

Group → Read, Execute

Others → Read, Execute

---

## 3. What does 644 mean?

Owner → Read, Write

Group → Read

Others → Read

---

## 4. Which command changes file permissions?

```bash
chmod
```

---

## 5. Which command changes file ownership?

```bash
chown
```

---

## 6. What is the purpose of umask?

It sets the default permissions for newly created files and directories.

---

## 7. Why should 777 be avoided?

Because it gives full permissions to everyone, which creates security risks.

---

# Hands-on Practice

```bash
touch demo.txt

ls -l

chmod 644 demo.txt

chmod 755 demo.txt

chmod +x demo.txt

sudo chown ubuntu demo.txt

sudo chgrp developers demo.txt

umask
```

---

# Conclusion

Linux file permissions are essential for securing systems and controlling access. A good understanding of permissions, ownership, and special permission bits is critical for Linux administration and DevOps roles.
