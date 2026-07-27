# Linux Interview Questions and Answers

This document contains commonly asked Linux interview questions for Linux Administrator, Cloud Engineer, AWS Engineer, and DevOps Engineer roles.

---

# Basic Linux

## 1. What is Linux?

Linux is an open-source operating system based on the Unix architecture. It is widely used for servers, cloud computing, and DevOps.

---

## 2. What are the advantages of Linux?

- Open Source
- Secure
- Stable
- Fast
- Multi-user
- Multitasking
- Lightweight

---

## 3. What is Kernel?

The Kernel is the core of the Linux operating system. It acts as a bridge between hardware and software.

---

## 4. What is Shell?

A Shell is a command-line interface that allows users to communicate with the Linux Kernel.

---

## 5. What are Linux distributions?

Examples:

- Ubuntu
- CentOS
- Red Hat Enterprise Linux
- Debian
- Fedora
- Amazon Linux
- Kali Linux

---

# Linux Commands

## 6. Which command displays the current directory?

```bash
pwd
```

---

## 7. Which command lists files?

```bash
ls
```

---

## 8. Which command creates a directory?

```bash
mkdir directory_name
```

---

## 9. Which command removes a directory?

```bash
rmdir directory_name
```

---

## 10. Which command creates an empty file?

```bash
touch file.txt
```

---

## 11. Which command displays file contents?

```bash
cat file.txt
```

---

## 12. Which command copies files?

```bash
cp source destination
```

---

## 13. Which command moves files?

```bash
mv source destination
```

---

## 14. Which command deletes files?

```bash
rm file.txt
```

---

## 15. Which command clears the terminal?

```bash
clear
```

---

# File Permissions

## 16. What does chmod do?

It changes file or directory permissions.

---

## 17. What does chmod 755 mean?

- Owner: Read, Write, Execute
- Group: Read, Execute
- Others: Read, Execute

---

## 18. What does chmod 777 mean?

Everyone has Read, Write, and Execute permissions.

---

## 19. Which command changes file ownership?

```bash
chown
```

---

## 20. What does chgrp do?

Changes the group ownership of a file.

---

# User Management

## 21. Create a user

```bash
sudo useradd devops
```

---

## 22. Set password

```bash
sudo passwd devops
```

---

## 23. Delete user

```bash
sudo userdel devops
```

---

## 24. Create group

```bash
sudo groupadd developers
```

---

## 25. Add user to group

```bash
sudo usermod -aG developers devops
```

---

# Process Management

## 26. What is a process?

A process is a running program.

---

## 27. Which command shows running processes?

```bash
ps -ef
```

---

## 28. Which command shows live processes?

```bash
top
```

---

## 29. Kill a process

```bash
kill PID
```

---

## 30. Force kill

```bash
kill -9 PID
```

---

# Networking

## 31. Display IP Address

```bash
ip addr
```

---

## 32. Test network connectivity

```bash
ping google.com
```

---

## 33. Display routing table

```bash
ip route
```

---

## 34. Display open ports

```bash
ss -tuln
```

---

## 35. Display hostname

```bash
hostname
```

---

# Storage

## 36. Display block devices

```bash
lsblk
```

---

## 37. Display disk usage

```bash
df -h
```

---

## 38. Display filesystem usage

```bash
du -sh
```

---

## 39. Mount a partition

```bash
mount
```

---

## 40. Unmount a partition

```bash
umount
```

---

# Archiving

## 41. Create tar archive

```bash
tar -cvf backup.tar folder
```

---

## 42. Extract tar archive

```bash
tar -xvf backup.tar
```

---

## 43. Compress using gzip

```bash
gzip file.txt
```

---

## 44. Extract gzip

```bash
gunzip file.txt.gz
```

---

# Shell Scripting

## 45. Execute script

```bash
./script.sh
```

---

## 46. Give execute permission

```bash
chmod +x script.sh
```

---

## 47. Display current shell

```bash
echo $SHELL
```

---

## 48. Read user input

```bash
read name
```

---

## 49. First line of Bash script

```bash
#!/bin/bash
```

---

# Services

## 50. Check service status

```bash
systemctl status ssh
```

---

## 51. Start a service

```bash
sudo systemctl start nginx
```

---

## 52. Stop a service

```bash
sudo systemctl stop nginx
```

---

## 53. Restart a service

```bash
sudo systemctl restart nginx
```

---

## 54. Enable a service

```bash
sudo systemctl enable nginx
```

---

# Logs

## 55. View system logs

```bash
journalctl
```

---

## 56. View last 20 log lines

```bash
tail -20 /var/log/syslog
```

---

# Interview Scenario Questions

## 57. A server is slow. What will you check?

- CPU Usage (`top`)
- Memory (`free -h`)
- Disk (`df -h`)
- Running Processes (`ps -ef`)
- Logs (`journalctl`)

---

## 58. Root filesystem is full. What will you do?

- Check disk usage using `df -h`
- Find large files using `du`
- Delete unnecessary files
- Archive old logs

---

## 59. User cannot log in. What will you check?

- User exists
- Password
- SSH service
- Home directory
- Permissions

---

## 60. Website is not opening. What will you check?

- Network connectivity
- Web server status
- Firewall
- Open ports
- Logs

---

# Quick Revision Commands

```bash
pwd
ls -la
cd
mkdir
touch
cp
mv
rm
cat
head
tail
grep
find
chmod
chown
useradd
passwd
groupadd
usermod
ps -ef
top
kill
jobs
ip addr
ip route
ping
ss -tuln
hostname
lsblk
df -h
du -sh
mount
umount
tar
gzip
systemctl
journalctl
```

---

# Conclusion

Mastering these Linux interview questions and commands will help you prepare for interviews related to Linux Administration, Cloud Computing, AWS, and DevOps. Practice these commands on a Linux machine so that you can explain and demonstrate them confidently during technical interviews.
