# Chapter 7 - Archiving and Compression

# Introduction

Archiving and Compression are commonly used in Linux to combine multiple files into a single archive and reduce file size for storage, backup, and transfer.

- **Archiving** combines multiple files into one file.
- **Compression** reduces the size of files.

These operations are widely used by Linux Administrators and DevOps Engineers for backups, deployments, and log management.

---

# What is Archiving?

Archiving means combining multiple files and directories into a single file without reducing their size.

Linux uses the **tar** command for archiving.

Example:

```
Documents/
Images/
Notes/

↓

backup.tar
```

---

# What is Compression?

Compression reduces the size of a file to save disk space and improve transfer speed.

Common compression formats:

- .gz
- .bz2
- .xz
- .zip

---

# tar Command

The **tar** command is used to create, extract, and manage archive files.

Syntax

```bash
tar [options] archive-name files
```

---

# Important tar Options

| Option | Description |
|---------|-------------|
| -c | Create archive |
| -x | Extract archive |
| -v | Verbose output |
| -f | Archive file name |
| -t | List archive contents |
| -z | Gzip compression |
| -j | Bzip2 compression |
| -J | XZ compression |

---

# Create Archive

```bash
tar -cvf backup.tar Documents
```

Example Output

```
Documents/
Documents/file1.txt
Documents/file2.txt
```

---

# Archive Multiple Directories

```bash
tar -cvf backup.tar Documents Downloads Pictures
```

---

# List Archive Contents

```bash
tar -tvf backup.tar
```

---

# Extract Archive

```bash
tar -xvf backup.tar
```

Extract into another directory

```bash
tar -xvf backup.tar -C /home/ubuntu/
```

---

# Gzip Compression

Create compressed archive

```bash
tar -czvf backup.tar.gz Documents
```

Extract

```bash
tar -xzvf backup.tar.gz
```

---

# Bzip2 Compression

Create

```bash
tar -cjvf backup.tar.bz2 Documents
```

Extract

```bash
tar -xjvf backup.tar.bz2
```

---

# XZ Compression

Create

```bash
tar -cJvf backup.tar.xz Documents
```

Extract

```bash
tar -xJvf backup.tar.xz
```

---

# gzip Command

Compress file

```bash
gzip file.txt
```

Output

```
file.txt.gz
```

Decompress

```bash
gunzip file.txt.gz
```

---

# bzip2 Command

Compress

```bash
bzip2 file.txt
```

Decompress

```bash
bunzip2 file.txt.bz2
```

---

# xz Command

Compress

```bash
xz file.txt
```

Decompress

```bash
unxz file.txt.xz
```

---

# zip Command

Create ZIP archive

```bash
zip backup.zip file1.txt file2.txt
```

Extract ZIP

```bash
unzip backup.zip
```

---

# Compare Compression Formats

| Format | Extension | Speed | Compression |
|----------|-----------|--------|-------------|
| gzip | .gz | Fast | Good |
| bzip2 | .bz2 | Medium | Better |
| xz | .xz | Slow | Best |
| zip | .zip | Fast | Good |

---

# Backup Example

Create project folder

```bash
mkdir project
```

Create files

```bash
touch project/file1.txt
touch project/file2.txt
```

Create archive

```bash
tar -cvf project.tar project
```

Compress archive

```bash
gzip project.tar
```

Verify

```bash
ls -lh
```

Extract

```bash
gunzip project.tar.gz

tar -xvf project.tar
```

---

# Best Practices

- Compress backups before storing.
- Verify archive contents after creation.
- Keep multiple backup copies.
- Use meaningful archive names.
- Test restoration regularly.

---

# Summary

In this chapter, we learned:

- Archiving
- Compression
- tar command
- gzip
- bzip2
- xz
- zip
- Backup process

---

# Interview Questions

## 1. What is the difference between Archiving and Compression?

- Archiving combines multiple files into one file.
- Compression reduces file size.

---

## 2. Which command is used for archiving?

```bash
tar
```

---

## 3. Which command creates a compressed tar archive?

```bash
tar -czvf backup.tar.gz folder
```

---

## 4. Which command extracts a tar archive?

```bash
tar -xvf backup.tar
```

---

## 5. Which compression format provides the highest compression?

```
xz
```

---

## 6. Which command compresses a single file?

```bash
gzip file.txt
```

---

## 7. Which command extracts a ZIP archive?

```bash
unzip backup.zip
```

---

# Hands-on Lab

## Objective

Learn how to archive and compress files using Linux commands.

### Step 1

Create a directory

```bash
mkdir LinuxBackup
```

### Step 2

Create sample files

```bash
touch LinuxBackup/file1.txt
touch LinuxBackup/file2.txt
touch LinuxBackup/file3.txt
```

### Step 3

Create archive

```bash
tar -cvf LinuxBackup.tar LinuxBackup
```

### Step 4

Compress archive

```bash
gzip LinuxBackup.tar
```

### Step 5

View compressed file

```bash
ls -lh
```

### Step 6

Extract archive

```bash
gunzip LinuxBackup.tar.gz

tar -xvf LinuxBackup.tar
```

### Expected Output

```
LinuxBackup/
file1.txt
file2.txt
file3.txt
```

---

# Conclusion

Archiving and compression are essential Linux skills used for backups, software deployment, log management, and data transfer. Mastering tools such as **tar**, **gzip**, **bzip2**, **xz**, and **zip** is important for every Linux Administrator, Cloud Engineer, and DevOps Engineer.
