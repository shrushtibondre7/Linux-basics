# Chapter 4 - User and Group Management

# Introduction

Linux is a multi-user operating system. Multiple users can work on the same system securely at the same time.

Every user has their own username, password, home directory, and permissions.

User and Group Management is one of the most important responsibilities of a Linux Administrator.

---

# Types of Users

## 1. Root User

- Superuser of Linux
- Has complete control over the operating system
- User ID (UID) = 0
- Can perform all administrative tasks

Example:

```bash
sudo su
```

---

## 2. System Users

- Created automatically during software installation
- Used by services and applications
- Cannot normally log in

Examples:

- apache
- nginx
- mysql
- nobody

---

## 3. Regular Users

Users created for daily work.

Examples:

- ubuntu
- shrushti
- devops

---

# What is UID?

UID stands for User ID.

Every user has a unique UID.

Example

```bash
id ubuntu
```

Output

```
uid=1000(ubuntu)
gid=1000(ubuntu)
groups=1000(ubuntu)
```

---

# What is GID?

GID stands for Group ID.

Each group has its own unique identification number.

Check GID

```bash
id
```

---

# Important User Files

## /etc/passwd

Stores user account information.

View

```bash
cat /etc/passwd
```

Example

```
ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash
```

Fields

- Username
- Password Placeholder
- UID
- GID
- Comment
- Home Directory
- Login Shell

---

## /etc/shadow

Stores encrypted passwords.

View

```bash
sudo cat /etc/shadow
```

---

## /etc/group

Stores group information.

View

```bash
cat /etc/group
```

---

# User Management Commands

## Create User

```bash
sudo useradd devops
```

---

## Create User with Home Directory

```bash
sudo adduser devops
```

Difference

| useradd | adduser |
|----------|----------|
| Low-level command | User-friendly command |
| Doesn't ask questions | Interactive |
| Doesn't create home directory automatically (depends on distro) | Creates home directory |

---

## Set Password

```bash
sudo passwd devops
```

---

## Change Password

```bash
passwd
```

---

## Delete User

```bash
sudo userdel devops
```

Delete User with Home Directory

```bash
sudo userdel -r devops
```

---

## Modify User

```bash
sudo usermod
```

Example

Add user to group

```bash
sudo usermod -aG docker devops
```

Unlock User

```bash
sudo usermod -U devops
```

Lock User

```bash
sudo usermod -L devops
```

---

# Group Management

## Create Group

```bash
sudo groupadd developers
```

---

## Delete Group

```bash
sudo groupdel developers
```

---

## Rename Group

```bash
sudo groupmod -n cloud developers
```

---

## Add User to Group

```bash
sudo usermod -aG developers devops
```

---

## Remove User from Group

```bash
sudo gpasswd -d devops developers
```

---

# Check User Information

Current User

```bash
whoami
```

Current User ID

```bash
id
```

Groups

```bash
groups
```

Check User Details

```bash
finger devops
```

---

# Switch User

```bash
su username
```

Example

```bash
su devops
```

Switch to Root

```bash
sudo su
```

Exit

```bash
exit
```

---

# Home Directory

Every user has a home directory.

Example

```
/home/devops
```

Root User

```
/root
```

Go to Home Directory

```bash
cd ~
```

---

# Default Files Created for a User

```
.bashrc
.profile
.bash_logout
```

Hidden files start with a dot (.).

View hidden files

```bash
ls -la
```

---

# Best Practices

- Use strong passwords.
- Avoid logging in as root.
- Give users only the required permissions.
- Remove unused accounts.
- Use groups instead of assigning permissions individually.
- Review user accounts regularly.

---

# Summary

In this chapter, we learned:

- Types of users
- UID and GID
- User management
- Group management
- User information files
- Home directories
- Important commands

---

# Interview Questions

## 1. What is the difference between Root User and Normal User?

Root user has full administrative privileges, while a normal user has limited permissions.

---

## 2. What is UID?

UID (User ID) is a unique number assigned to every user.

---

## 3. Which file stores user account information?

```
/etc/passwd
```

---

## 4. Which file stores encrypted passwords?

```
/etc/shadow
```

---

## 5. Which command creates a new user?

```bash
useradd
```

or

```bash
adduser
```

---

## 6. What is the difference between useradd and adduser?

- useradd is a low-level command.
- adduser is interactive and creates the home directory automatically on most distributions.

---

## 7. Which command displays current user information?

```bash
id
```

---

## 8. How do you add a user to a group?

```bash
sudo usermod -aG developers devops
```

---

# Hands-on Practice

```bash
sudo adduser devops

sudo passwd devops

sudo groupadd developers

sudo usermod -aG developers devops

id devops

groups devops

cat /etc/passwd

cat /etc/group

sudo userdel -r devops
```

---

# Conclusion

User and Group Management is a core Linux administration skill. Understanding users, groups, permissions, and authentication is essential for system administration, Cloud Computing, and DevOps environments.
