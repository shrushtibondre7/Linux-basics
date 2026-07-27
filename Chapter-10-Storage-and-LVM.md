# Chapter 10 - Storage Management & LVM

# Introduction

Storage Management is the process of organizing, managing, and maintaining storage devices such as hard disks, SSDs, and partitions.

Linux provides powerful tools to create partitions, mount file systems, manage Logical Volume Manager (LVM), and configure swap space.

Storage management is an essential skill for Linux Administrators, Cloud Engineers, and DevOps Engineers.

---

# Storage Concepts

## Hard Disk

A hard disk (HDD) or SSD stores operating system files, applications, and user data.

Examples:

- HDD
- SSD
- NVMe SSD

---

## Partition

A partition is a logical section of a disk.

Example

```
Disk
│
├── Partition 1
├── Partition 2
└── Partition 3
```

---

## File System

A file system organizes how data is stored and retrieved.

Common Linux file systems:

- ext4
- xfs
- btrfs

Display mounted file systems

```bash
df -Th
```

---

# View Storage Information

List Block Devices

```bash
lsblk
```

Display Disk Usage

```bash
df -h
```

Display File System Type

```bash
df -Th
```

Display Partition Information

```bash
sudo fdisk -l
```

---

# Creating a Partition

Start partition utility

```bash
sudo fdisk /dev/sdb
```

Useful commands inside fdisk

| Command | Description |
|----------|-------------|
| n | New Partition |
| p | Primary Partition |
| w | Save Changes |
| q | Quit Without Saving |
| d | Delete Partition |

---

# Create File System

Format partition using ext4

```bash
sudo mkfs.ext4 /dev/sdb1
```

Format using xfs

```bash
sudo mkfs.xfs /dev/sdb1
```

---

# Mount File System

Create mount directory

```bash
sudo mkdir /data
```

Mount partition

```bash
sudo mount /dev/sdb1 /data
```

Verify

```bash
df -h
```

---

# Permanent Mount

Edit

```text
/etc/fstab
```

Example

```text
/dev/sdb1   /data   ext4   defaults   0 0
```

Apply changes

```bash
sudo mount -a
```

---

# Unmount File System

```bash
sudo umount /data
```

---

# LVM (Logical Volume Manager)

LVM provides flexible disk management.

Advantages:

- Easy resizing
- Better storage management
- Snapshots
- Multiple disks can be combined

---

# LVM Components

## Physical Volume (PV)

Actual disk or partition.

Create PV

```bash
sudo pvcreate /dev/sdb1
```

View PV

```bash
sudo pvs
```

---

## Volume Group (VG)

Collection of Physical Volumes.

Create VG

```bash
sudo vgcreate vgdata /dev/sdb1
```

View VG

```bash
sudo vgs
```

---

## Logical Volume (LV)

Virtual partition created from Volume Group.

Create LV

```bash
sudo lvcreate -L 5G -n lvdata vgdata
```

View LV

```bash
sudo lvs
```

---

# Format Logical Volume

```bash
sudo mkfs.ext4 /dev/vgdata/lvdata
```

---

# Mount Logical Volume

```bash
sudo mkdir /lvdata

sudo mount /dev/vgdata/lvdata /lvdata
```

Verify

```bash
df -h
```

---

# Extend Logical Volume

Increase size

```bash
sudo lvextend -L +2G /dev/vgdata/lvdata
```

Resize File System

```bash
sudo resize2fs /dev/vgdata/lvdata
```

---

# Swap Space

Check Swap

```bash
swapon --show
```

Memory Information

```bash
free -h
```

Create Swap File

```bash
sudo fallocate -l 2G /swapfile
```

Set Permissions

```bash
sudo chmod 600 /swapfile
```

Format

```bash
sudo mkswap /swapfile
```

Enable

```bash
sudo swapon /swapfile
```

---

# Useful Commands

```bash
lsblk

df -h

df -Th

fdisk -l

mount

umount

mount -a

pvs

vgs

lvs

free -h

swapon --show
```

---

# Hands-on Lab

## Objective

Practice storage management and LVM commands.

### Step 1

Display storage

```bash
lsblk
```

---

### Step 2

Display disk usage

```bash
df -h
```

---

### Step 3

Create mount point

```bash
sudo mkdir /data
```

---

### Step 4

Mount partition

```bash
sudo mount /dev/sdb1 /data
```

---

### Step 5

Verify

```bash
df -h
```

---

### Step 6

Create Physical Volume

```bash
sudo pvcreate /dev/sdb1
```

---

### Step 7

Create Volume Group

```bash
sudo vgcreate vgdata /dev/sdb1
```

---

### Step 8

Create Logical Volume

```bash
sudo lvcreate -L 5G -n lvdata vgdata
```

---

### Step 9

Check LVM

```bash
sudo pvs

sudo vgs

sudo lvs
```

---

# Best Practices

- Always back up important data before modifying partitions.
- Verify mounted file systems after mounting.
- Use LVM for flexibility.
- Monitor disk usage regularly.
- Configure permanent mounts carefully.

---

# Summary

In this chapter, we learned:

- Hard Disk
- Partition
- File System
- Mount
- Unmount
- /etc/fstab
- Physical Volume (PV)
- Volume Group (VG)
- Logical Volume (LV)
- Swap Space

---

# Interview Questions

## 1. What is LVM?

LVM (Logical Volume Manager) provides flexible disk management in Linux.

---

## 2. What are the three components of LVM?

- Physical Volume (PV)
- Volume Group (VG)
- Logical Volume (LV)

---

## 3. Which command displays block devices?

```bash
lsblk
```

---

## 4. Which file stores permanent mount information?

```text
/etc/fstab
```

---

## 5. Which command mounts all file systems from fstab?

```bash
mount -a
```

---

## 6. Which command displays disk usage?

```bash
df -h
```

---

## 7. Which command displays swap information?

```bash
swapon --show
```

---

# Practice Commands

```bash
lsblk

df -h

df -Th

sudo fdisk -l

mount

umount

sudo pvs

sudo vgs

sudo lvs

free -h

swapon --show
```

---

# Conclusion

Storage Management and LVM are essential Linux administration skills. Understanding partitions, mounting, file systems, logical volumes, and swap space is important for managing Linux servers in cloud and enterprise environments.
