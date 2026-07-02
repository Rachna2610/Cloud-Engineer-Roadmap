# Day 3 Practical - Linux Permissions

## Objective

Learn how to:

- Check current user
- View file permissions
- Add execute permission
- Remove execute permission
- Read file contents

---

## Commands Used

### whoami

Shows the current logged-in user.

```bash
whoami
```

Output:

```text
rachna
```

---

### ls -l

Displays file permissions, owner, group, and file details.

```bash
ls -l
```

Example Output:

```text
-rw-r--r-- 1 rachna rachna 0 Jun 8 linux.txt
```

---

### chmod +x

Adds execute permission to a file.

```bash
chmod +x script.sh
```

Before:

```text
-rw-r--r--
```

After:

```text
-rwxr-xr-x
```

---

### chmod -x

Removes execute permission.

```bash
chmod -x script.sh
```

Before:

```text
-rwxr-xr-x
```

After:

```text
-rw-r--r--
```

---

### echo

Adds content to a file.

```bash
echo "Cloud Engineer Journey" > linux.txt
```

---

### cat

Displays file contents.

```bash
cat linux.txt
```

Output:

```text
Cloud Engineer Journey
```

---

## Practical Task Performed

Created a folder:

```bash
mkdir cloudlab
```

Created files:

```bash
touch linux.txt
touch aws.txt
touch script.sh
```

Checked current user:

```bash
whoami
```

Viewed permissions:

```bash
ls -l
```

Added execute permission:

```bash
chmod +x script.sh
```

Removed execute permission:

```bash
chmod -x script.sh
```

Added content:

```bash
echo "Cloud Engineer Journey" > linux.txt
```

Displayed content:

```bash
cat linux.txt
```

---

## What I Learned

- How to check the current user
- How to view Linux permissions
- How to add execute permission
- How to remove execute permission
- How to create and manage files
- Why permissions are important for AWS EC2 servers