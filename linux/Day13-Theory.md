# Day 13 – Archive and Compression in Linux

## Learning Objectives

After completing this topic, you will be able to:

- Understand archiving and compression.
- Learn why backups are important.
- Use tar, gzip, and zip commands.
- Extract compressed files.
- Understand real-world cloud backup scenarios.

---

# What is Archiving?

Archiving is the process of combining multiple files and directories into a single file.

An archive file makes it easier to:

- Store files
- Transfer files
- Create backups

Example:

Instead of sending 100 files individually, they can be combined into one archive file.

---

# What is Compression?

Compression is the process of reducing the size of a file.

Benefits include:

- Saves disk space
- Faster file transfer
- Faster backups
- Reduced storage costs

---

# Difference Between Archive and Compression

| Archive | Compression |
|----------|-------------|
| Combines multiple files into one | Reduces file size |
| Does not reduce size by itself | Reduces storage space |
| Created using `tar` | Created using `gzip`, `bzip2`, or `zip` |

---

# Why are Archives Used?

System administrators use archives for:

- System backups
- Database backups
- Application backups
- Log backups
- File transfers

---

# The tar Command

The `tar` command creates and extracts archive files.

### Create an Archive

```bash
tar -cvf backup.tar foldername
```

Options:

- `c` → Create archive
- `v` → Verbose output
- `f` → File name

Example:

```bash
tar -cvf project.tar project/
```

---

# Extract an Archive

```bash
tar -xvf backup.tar
```

Options:

- `x` → Extract
- `v` → Verbose
- `f` → File name

---

# gzip Compression

Compress a file:

```bash
gzip filename
```

Example:

```bash
gzip notes.txt
```

Result:

```
notes.txt.gz
```

---

# Decompress a File

```bash
gunzip notes.txt.gz
```

---

# Create a Compressed Archive

Archive and compress in one command:

```bash
tar -czvf backup.tar.gz foldername
```

Options:

- `c` → Create
- `z` → Compress using gzip
- `v` → Verbose
- `f` → File name

---

# Extract a Compressed Archive

```bash
tar -xzvf backup.tar.gz
```

---

# zip Command

Create a ZIP archive:

```bash
zip -r backup.zip foldername
```

Options:

- `r` → Recursive (include folders)

---

# Unzip Command

Extract a ZIP archive:

```bash
unzip backup.zip
```

---

# Common Archive Formats

| Extension | Description |
|-----------|-------------|
| `.tar` | Archive only |
| `.tar.gz` | Archive + Gzip compression |
| `.zip` | ZIP archive |
| `.gz` | Gzip compressed file |

---

# Why is Compression Important?

Advantages:

- Saves storage space
- Reduces network bandwidth
- Faster uploads
- Faster downloads
- Easier backups

---

# AWS Cloud Engineer Example

Suppose an EC2 server generates log files every day.

Instead of storing thousands of log files separately, a Cloud Engineer can:

1. Archive the logs.
2. Compress the archive.
3. Upload it to Amazon S3.

Example:

```bash
tar -czvf logs.tar.gz /var/log
```

This reduces storage usage and makes backups easier.

---

# Best Practices

- Compress old log files.
- Keep regular backups.
- Store backups on separate storage.
- Verify backup files after creation.
- Delete unnecessary old backups.

---

# Important Commands Summary

```bash
tar -cvf backup.tar foldername

tar -xvf backup.tar

gzip filename

gunzip filename.gz

tar -czvf backup.tar.gz foldername

tar -xzvf backup.tar.gz

zip -r backup.zip foldername

unzip backup.zip
```

---

# Interview Questions

### 1. What is archiving?

Archiving is the process of combining multiple files into a single file.

---

### 2. What is compression?

Compression reduces the size of files to save storage space.

---

### 3. Which command creates an archive?

```bash
tar -cvf backup.tar foldername
```

---

### 4. Which command extracts an archive?

```bash
tar -xvf backup.tar
```

---

### 5. Which command compresses a file?

```bash
gzip filename
```

---

### 6. What is the difference between `.tar` and `.tar.gz`?

- `.tar` is only an archive.
- `.tar.gz` is an archive that has been compressed using gzip.

---

### 7. Why do Cloud Engineers compress backups?

To reduce storage space, improve transfer speed, and lower storage costs.

---

### 8. Which command creates a compressed archive?

```bash
tar -czvf backup.tar.gz foldername
```

---

# Day 13 Summary

After completing Day 13, you should be able to:

- Understand archiving and compression.
- Create archive files.
- Compress and extract files.
- Use tar, gzip, zip, and unzip commands.
- Understand backup strategies used by Linux administrators and Cloud Engineers.