# Linux Hands-on Labs

This document contains practical Linux labs for beginners, Linux Administrators, Cloud Engineers, and DevOps Engineers.

---

# Lab 1 - Basic Linux Commands

## Objective

Learn basic Linux commands.

## Commands

```bash
pwd
ls
ls -la
whoami
hostname
date
cal
```

---

# Lab 2 - File and Directory Management

## Objective

Create and manage files and directories.

```bash
mkdir LinuxLab

cd LinuxLab

touch file1.txt

touch file2.txt

mkdir Notes

ls -l

cp file1.txt Notes/

mv file2.txt file3.txt

rm file3.txt
```

---

# Lab 3 - File Permissions

## Objective

Practice file permissions.

```bash
touch demo.txt

chmod 755 demo.txt

ls -l demo.txt

chmod 644 demo.txt

chmod 777 demo.txt
```

---

# Lab 4 - User Management

## Objective

Create users and groups.

```bash
sudo useradd devops

sudo passwd devops

sudo groupadd developers

sudo usermod -aG developers devops

id devops

groups devops
```

---

# Lab 5 - Process Management

## Objective

Manage running processes.

```bash
ps -ef

top

sleep 300 &

jobs

pidof sleep

kill PID
```

Replace **PID** with the actual Process ID.

---

# Lab 6 - Networking

## Objective

Practice networking commands.

```bash
hostname

hostnamectl

ip addr

ip route

ping google.com

ss -tuln

nslookup google.com
```

---

# Lab 7 - Storage Management

## Objective

View storage information.

```bash
lsblk

df -h

df -Th

mount

free -h
```

---

# Lab 8 - Archiving

## Objective

Create and extract archives.

```bash
mkdir Backup

touch Backup/file1.txt

touch Backup/file2.txt

tar -cvf backup.tar Backup

tar -tvf backup.tar

tar -xvf backup.tar
```

---

# Lab 9 - Compression

## Objective

Compress and extract files.

```bash
gzip backup.tar

gunzip backup.tar.gz

zip backup.zip Backup/*

unzip backup.zip
```

---

# Lab 10 - Shell Script

## Objective

Create and execute a shell script.

```bash
touch hello.sh

vim hello.sh
```

Add:

```bash
#!/bin/bash

echo "Hello Linux"
```

Execute:

```bash
chmod +x hello.sh

./hello.sh
```

---

# Lab 11 - Search Commands

```bash
find /home -name "*.txt"

grep "Linux" file.txt

sort names.txt

uniq names.txt
```

---

# Lab 12 - Disk Usage

```bash
df -h

du -sh *

du -sh /home
```

---

# Lab 13 - Package Management (Ubuntu)

```bash
sudo apt update

sudo apt upgrade

sudo apt install tree

tree
```

---

# Lab 14 - Services

```bash
systemctl status ssh

systemctl list-units --type=service

sudo systemctl restart ssh
```

---

# Lab 15 - Logs

```bash
journalctl

journalctl -xe

tail -20 /var/log/syslog
```

---

# Lab 16 - System Information

```bash
uname -a

lscpu

free -h

hostnamectl
```

---

# Lab 17 - Environment Variables

```bash
echo $HOME

echo $PATH

echo $SHELL

printenv
```

---

# Lab 18 - Scheduling Jobs

Create a cron job.

```bash
crontab -e
```

Example

```text
0 9 * * * echo "Good Morning"
```

Display cron jobs

```bash
crontab -l
```

---

# Lab 19 - File Ownership

```bash
sudo chown user:user file.txt

sudo chgrp developers file.txt

ls -l
```

---

# Lab 20 - Complete Linux Practice

Practice the following commands:

```bash
pwd

ls -la

mkdir project

cd project

touch app.txt

echo "Linux Practice" > app.txt

cat app.txt

chmod 755 app.txt

cp app.txt backup.txt

mv backup.txt final.txt

tar -cvf project.tar .

gzip project.tar

ls -lh

df -h

free -h

ip addr

ps -ef

top
```

---

# Mini Project

## Linux Server Setup

### Objective

Prepare a Linux server for a web application.

### Tasks

- Create a user named **developer**
- Create a group named **webteam**
- Add the user to the group
- Create `/var/www/project`
- Give appropriate permissions
- Install Nginx or Apache
- Start the web server
- Verify that it is running
- Check firewall status
- Create a backup using `tar`

---

# Expected Skills After Completing These Labs

- Linux Commands
- User Management
- File Permissions
- Networking
- Storage Management
- Process Management
- Shell Scripting
- Archiving
- Package Management
- Service Management

---

# Conclusion

These hands-on labs provide practical Linux experience commonly required for Linux Administrator, AWS, Cloud, and DevOps roles. Practice every lab on a Linux virtual machine or cloud instance to build confidence before interviews.
