# Day 12 – User and Group Management in Linux

## Learning Objectives

After completing this topic, you will be able to:

- Understand users and groups in Linux.
- Learn different types of users.
- Manage users and groups using Linux commands.
- Understand file ownership and permissions.
- Learn why user management is important in cloud environments.

---

# What is User Management?

User management is the process of creating, modifying, deleting, and managing user accounts in a Linux system.

It ensures that only authorized users can access the system and perform specific tasks.

---

# Why is User Management Important?

Every Linux server can have multiple users.

Examples:

- System Administrator
- Developer
- Database Administrator
- DevOps Engineer
- Application User

Each user should have only the permissions required for their work.

---

# Types of Users

## 1. Root User

The root user is the superuser of Linux.

Characteristics:

- Has complete control over the system.
- Can access all files.
- Can install or remove software.
- Can create or delete users.

Example:

```bash
sudo
```

---

## 2. Normal User

A normal user has limited permissions.

They can:

- Create files
- Edit files
- Run programs

They cannot:

- Install software
- Modify system files
- Manage other users

without administrator privileges.

---

## 3. System Users

System users are created automatically by Linux.

They run services such as:

- nginx
- mysql
- apache
- cron

These users usually cannot log in.

---

# What is a Group?

A group is a collection of users.

Groups make permission management easier.

Example:

```
Developers Group
├── Rachna
├── Rahul
└── Priya
```

Instead of assigning permissions to each user individually, permissions can be assigned to the entire group.

---

# Home Directory

Every normal user has a home directory.

Example:

```
/home/rachna
```

This directory stores:

- Documents
- Downloads
- Configuration files

---

# Important Commands

## Display Current User

```bash
whoami
```

Example output:

```
rachna
```

---

## Display User ID

```bash
id
```

Shows:

- User ID (UID)
- Group ID (GID)
- Groups

---

## Display Logged-in Users

```bash
who
```

Shows all currently logged-in users.

---

## Create a New User

```bash
sudo adduser username
```

Example:

```bash
sudo adduser testuser
```

---

## Delete a User

```bash
sudo deluser username
```

Example:

```bash
sudo deluser testuser
```

---

## Create a Group

```bash
sudo groupadd developers
```

---

## Add User to a Group

```bash
sudo usermod -aG developers rachna
```

Options:

- `-a` → Append
- `-G` → Group

---

# File Ownership

Every file belongs to:

- One User (Owner)
- One Group

Example:

```
Owner: rachna
Group: developers
```

Ownership helps Linux decide who can read, write, or execute files.

---

# Why User Management is Important in AWS?

Suppose a company has:

- 20 Developers
- 5 DevOps Engineers
- 2 Database Administrators

Instead of giving everyone root access:

- Developers receive limited permissions.
- DevOps Engineers receive administrative privileges.
- Database Administrators manage only databases.

This improves security and reduces the risk of accidental system changes.

---

# Best Practices

- Do not use the root account for daily work.
- Give users only the permissions they need.
- Use groups to manage permissions.
- Remove inactive users.
- Regularly review user accounts.

---

# Important Commands Summary

```bash
whoami

id

who

sudo adduser username

sudo deluser username

sudo groupadd groupname

sudo usermod -aG groupname username
```

---

# Interview Questions

### 1. What is user management?

User management is the process of creating, modifying, and managing user accounts in Linux.

---

### 2. Who is the root user?

The root user is the superuser with complete control over the Linux system.

---

### 3. Which command displays the current user?

```bash
whoami
```

---

### 4. Which command displays user information?

```bash
id
```

---

### 5. What is a group?

A group is a collection of users that share common permissions.

---

### 6. Why are groups used?

Groups simplify permission management by allowing permissions to be assigned to multiple users at once.

---

### 7. Which command creates a new user?

```bash
sudo adduser username
```

---

### 8. Why is user management important in cloud computing?

It improves security by ensuring users have only the permissions necessary for their roles, reducing unauthorized access and accidental changes.

---

# Day 12 Summary

After completing Day 12, you should be able to:

- Understand Linux users and groups.
- Differentiate between root, normal, and system users.
- Manage users and groups.
- Understand file ownership.
- Apply user management best practices in Linux and AWS EC2.