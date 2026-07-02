# Day 1 - Basic Linux Commands

## 1. pwd (Print Working Directory)

### Purpose
Shows the current directory (location) where you are working.

### Syntax
pwd

### Example
pwd

### Output
/home/rachna/CloudPractice

### Use Case
Used to check your current location in the Linux file system.

---

## 2. ls (List)

### Purpose
Displays files and folders in the current directory.

### Syntax
ls

### Example
ls

### Output
AWS  Linux  Networking

### Use Case
Used to view available files and folders.

### Common Options

ls -l
Shows detailed information.

ls -a
Shows hidden files and folders.

---

## 3. mkdir (Make Directory)

### Purpose
Creates a new directory (folder).

### Syntax
mkdir folder_name

### Example
mkdir Linux

### Output
Creates a folder named Linux.

### Use Case
Used to organize files and create project structures.

---

## 4. cd (Change Directory)

### Purpose
Moves from one directory to another.

### Syntax
cd directory_name

### Example
cd Linux

### Use Case
Used to navigate between folders.

### Useful Variations

cd ..
Move one folder back.

cd ~
Move to home directory.

cd /
Move to root directory.

---

# Summary

| Command | Full Form | Purpose |
|----------|-----------|----------|
| pwd | Print Working Directory | Shows current location |
| ls | List | Shows files and folders |
| mkdir | Make Directory | Creates a folder |
| cd | Change Directory | Moves between folders |


# Day 2 - Linux File Management

## File

A file is used to store data.

Examples:
- notes.txt
- aws.txt
- app.py
- image.jpg

---

## Directory

A directory (folder) is used to store files and folders.

Examples:
- Linux
- AWS
- Projects

---

## File vs Directory

| File | Directory |
|--------|-----------|
| Stores data | Stores files and folders |
| notes.txt | Linux |
| app.py | AWS |

---

## Path

A path is the location of a file or directory.

Example:

/home/rachna/CloudPractice/day2

---

## Absolute Path

The complete path starting from the root directory (/).

Example:

/home/rachna/CloudPractice/day2

Characteristics:
- Starts with /
- Full location
- Works from anywhere

---

## Relative Path

The path relative to the current location.

Example:

cd Linux

Characteristics:
- Does not start with /
- Depends on current location

---

# Commands

## touch

Purpose:
Creates a new file.

Syntax:

touch filename

Example:

touch notes.txt

---

## cat

Purpose:
Displays file content.

Syntax:

cat filename

Example:

cat notes.txt

---

## cp

Purpose:
Copies files.

Syntax:

cp source destination

Example:

cp notes.txt backup.txt

---

## mv

Purpose:
Moves or renames files.

Syntax:

mv source destination

Rename Example:

mv notes.txt linux_notes.txt

Move Example:

mv notes.txt Documents/

---

## rm

Purpose:
Deletes files.

Syntax:

rm filename

Example:

rm notes.txt

Note:
Deletes permanently.

---

## rmdir

Purpose:
Deletes empty directories.

Syntax:

rmdir foldername

Example:

rmdir Test

---

# Commands Summary

touch  -> Create file

cat    -> View file content

cp     -> Copy file

mv     -> Move/Rename file

rm     -> Delete file

rmdir  -> Delete empty folder

---

# Practical Commands Used

touch notes.txt
touch aws.txt
touch linux.txt

cat notes.txt

cp notes.txt backup.txt

mv backup.txt linux_backup.txt

mkdir Documents

mv notes.txt Documents/

rm aws.txt

mkdir Test

rmdir Test