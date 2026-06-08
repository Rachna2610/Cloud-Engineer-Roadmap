# Linux File System

## Introduction

The Linux File System is the way Linux organizes and stores files and directories. Everything in Linux is organized in a hierarchical structure starting from the root directory (/).

Unlike Windows, Linux does not use drive letters such as C: or D:. Instead, all files and folders are connected under a single root directory.

---

## Linux Directory Structure

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── opt
├── proc
├── root
├── tmp
├── usr
└── var
```

The symbol `/` represents the Root Directory.

---

## Root Directory (/)

The root directory is the top-most directory in Linux.

All other directories and files are stored inside it.

Example:

```text
/
```

---

## Important Directories in Linux

### 1. /bin

Contains essential command binaries used by all users.

Examples:
- ls
- cp
- mv
- mkdir

---

### 2. /boot

Contains files needed to start the operating system.

Examples:
- Linux Kernel
- Boot Loader Files

---

### 3. /dev

Contains device files.

Examples:
- Hard Drives
- USB Devices
- Printers

---

### 4. /etc

Contains system configuration files.

Examples:
- User account information
- Network settings
- Service configurations

---

### 5. /home

Stores personal files of users.

Example:

```text
/home/rachna
```

Each user has a separate home directory.

---

### 6. /root

Home directory of the root (administrator) user.

Example:

```text
/root
```

---

### 7. /tmp

Stores temporary files.

Files may be deleted automatically when the system restarts.

---

### 8. /usr

Contains user programs and applications.

Examples:
- Installed software
- Libraries
- Documentation

---

### 9. /var

Stores variable data.

Examples:
- Logs
- Database files
- Email files

---

### 10. /media

Used for removable devices.

Examples:
- USB Drives
- CDs
- DVDs

---

## Absolute Path

An absolute path starts from the root directory.

Example:

```text
/home/rachna/Documents/file.txt
```

---

## Relative Path

A relative path starts from the current directory.

Example:

```text
Documents/file.txt
```

---

## Commands for Navigating the File System

### pwd

Displays current directory.

Example:

```bash
pwd
```

---

### ls

Lists files and folders.

Example:

```bash
ls
```

---

### cd

Changes directory.

Example:

```bash
cd /home
```

---

## Advantages of Linux File System

- Organized structure
- Better security
- Easy file management
- Efficient storage
- Supports multiple users

---

## Key Points to Remember

- Linux uses a hierarchical file structure.
- The root directory is represented by `/`.
- Everything starts from the root directory.
- Linux does not use drive letters like Windows.
- `/home` stores user files.
- `/etc` stores configuration files.
- `/var` stores logs and variable data.

---

## Interview Questions

### Q1. What is the root directory in Linux?

The root directory (/) is the top-most directory from which all other directories originate.

### Q2. What is the purpose of the /home directory?

It stores personal files and folders of users.

### Q3. What is stored in the /etc directory?

System configuration files are stored in the /etc directory.

### Q4. What is the difference between absolute and relative paths?

Absolute path starts from the root directory, while relative path starts from the current directory.

### Q5. Does Linux use drive letters like Windows?

No, Linux uses a single hierarchical file system starting from the root directory (/).