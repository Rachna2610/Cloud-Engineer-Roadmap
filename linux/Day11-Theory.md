# Day 11 – Disk & Storage Management in Linux

## Learning Objectives

After completing this topic, you will be able to:

- Understand Linux storage devices.
- Check disk usage and free space.
- Monitor mounted file systems.
- Understand partitions.
- Learn commonly used storage commands.
- Understand storage management on AWS EC2.

---

# What is Disk Management?

Disk Management is the process of managing storage devices, partitions, and available disk space in a Linux system.

It helps ensure that enough storage is available for applications, logs, databases, and user files.

---

# Why is Disk Management Important?

Every Linux server stores:

- Operating System
- Application Files
- User Data
- Log Files
- Databases
- Backups

If storage becomes full, applications may stop working or the server may become unstable.

---

# Storage Devices in Linux

Common storage devices include:

- Hard Disk Drive (HDD)
- Solid State Drive (SSD)
- NVMe SSD
- USB Drives
- Cloud Storage Volumes

In AWS EC2, storage is usually provided by **Amazon EBS (Elastic Block Store)**.

---

# Partitions

A partition divides a physical disk into smaller logical sections.

Each partition can contain its own file system.

Example:

```
Disk
├── Partition 1
├── Partition 2
└── Partition 3
```

---

# File System

A file system organizes how data is stored on a partition.

Common Linux file systems:

- ext4
- XFS
- Btrfs

Without a file system, Linux cannot store files.

---

# Mounted File System

Before Linux can use a storage device, it must be mounted.

Mounting connects the storage device to a directory.

Example:

```
Disk
   ↓
Mounted to
   ↓
/home
```

---

# Checking Disk Space

Display disk usage:

```bash
df -h
```

Options:

- `d` → Disk
- `f` → File System
- `-h` → Human-readable format

Shows:

- Total Size
- Used Space
- Available Space
- Mount Point

---

# Checking Directory Size

Display directory size:

```bash
du -sh directory_name
```

Options:

- `d` → Disk Usage
- `-s` → Summary
- `-h` → Human-readable

Example:

```bash
du -sh Documents
```

---

# Listing Storage Devices

Display block devices:

```bash
lsblk
```

Shows:

- Disks
- Partitions
- Mount Points

Example output:

```
sda
├── sda1
└── sda2
```

---

# Checking Mounted File Systems

Display mounted file systems:

```bash
mount
```

This command lists all currently mounted storage devices.

---

# Finding Free Space

Useful commands:

```bash
df -h
```

```bash
du -sh *
```

These commands help identify where storage is being used.

---

# AWS Cloud Engineer Example

Suppose an EC2 instance becomes slow because the disk is full.

A Cloud Engineer would:

1. Check available disk space.

```bash
df -h
```

2. Find large directories.

```bash
du -sh /*
```

3. Identify mounted disks.

```bash
lsblk
```

4. Delete unnecessary files or attach a larger EBS volume.

---

# Important Commands

```bash
df -h

du -sh directory_name

lsblk

mount
```

---

# Interview Questions

### 1. What is disk management?

Disk management is the process of monitoring and managing storage devices and available disk space.

---

### 2. Which command checks disk space?

```bash
df -h
```

---

### 3. Which command checks directory size?

```bash
du -sh directory_name
```

---

### 4. Which command lists storage devices?

```bash
lsblk
```

---

### 5. What is a partition?

A partition is a logical division of a physical disk.

---

### 6. What is a file system?

A file system organizes how data is stored and accessed on a storage device.

---

### 7. What does the `df` command display?

It displays disk space usage for mounted file systems.

---

### 8. Why is storage management important?

Storage management prevents servers from running out of space, ensures application stability, and helps maintain system performance.

---

# Day 11 Summary

After completing Day 11, you should be able to:

- Understand Linux storage concepts.
- Check available disk space.
- Monitor directory sizes.
- Identify storage devices.
- Understand partitions and file systems.
- Apply storage management techniques on Linux and AWS EC2.