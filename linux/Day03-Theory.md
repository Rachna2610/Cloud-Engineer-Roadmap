# Day 3 - Linux Users, Groups, Permissions & Ownership

## Why Permissions Matter

Linux permissions control:

- Who can read files
- Who can modify files
- Who can execute programs
- Who owns files

Permissions are important in:

- AWS EC2
- Azure Virtual Machines
- Google Cloud VMs
- Docker Containers
- Linux Servers

---

# User

A user is an account that can log in and use Linux.

Examples:

- rachna
- ubuntu
- ec2-user
- root

A user can:

- Create files
- Delete files
- Run commands
- Execute programs

Example:

touch notes.txt

The user who creates a file usually becomes its owner.

---

# Root User

Root is the administrator of Linux.

Root has full control over the system.

Root can:

- Read any file
- Modify any file
- Delete any file
- Install software
- Create users
- Change permissions

Example:

sudo apt update

sudo apt install nginx

The sudo command temporarily gives root privileges.

---

# Group

A group is a collection of users.

Examples:

- Developers
- Admins
- CloudTeam

Benefits:

- Easier permission management
- Multiple users can share access

Example:

Developers Group
├── Rachna
├── Aman
└── Priya

---

# Ownership

Every file and directory has:

1. Owner
2. Group

Example:

notes.txt

Owner : rachna

Group : developers

Ownership helps Linux determine who can access a file.

---

# Linux Permissions

Linux uses three permissions:

## Read (r)

Symbol:

r

Purpose:

Allows viewing file contents.

Example:

cat notes.txt

---

## Write (w)

Symbol:

w

Purpose:

Allows modifying file contents.

Example:

echo "Hello" > notes.txt

---

## Execute (x)

Symbol:

x

Purpose:

Allows running a file as a program.

Example:

./script.sh

---

# Permission Categories

Linux checks permissions for three categories:

## User

Owner of the file.

Example:

rachna

---

## Group

Members of the file's group.

Example:

developers

---

## Others

Everyone else who is not the owner or group member.

---

# Permission Structure

Example:

-rw-r--r--

Breakdown:

rw-   r--   r--

Owner  -> Read + Write

Group  -> Read

Others -> Read

---

Example:

rwxr-xr-x

Owner  -> Read + Write + Execute

Group  -> Read + Execute

Others -> Read + Execute

---

# ls -l

Purpose:

Displays detailed information about files.

Command:

ls -l

Example Output:

-rw-r--r-- 1 rachna developers 100 Jun 3 notes.txt

Important Fields:

-rw-r--r--  -> Permissions

rachna      -> Owner

developers  -> Group

---

# chmod

Purpose:

Changes file permissions.

Command:

chmod permissions filename

Example:

chmod 755 script.sh

Important:

chmod = Change Permissions

---

# chown

Purpose:

Changes file ownership.

Command:

chown user filename

Example:

chown ubuntu notes.txt

Important:

chown = Change Owner

---

# whoami

Purpose:

Shows the current logged-in user.

Command:

whoami

Example Output:

rachna

---

# Cloud Engineering Usage

Cloud Engineers use permissions to:

- Secure AWS EC2 servers
- Control user access
- Protect application files
- Run scripts safely
- Manage production environments

---

# Commands Learned

whoami

ls -l

chmod

chown

---

# Key Concepts

User      -> Account using Linux

Root      -> Administrator

Group     -> Collection of users

Owner     -> User who owns a file

Permissions:
r -> Read
w -> Write
x -> Execute

Categories:
User
Group
Others

chmod -> Change Permissions

chown -> Change Ownership

whoami -> Show Current User

ls -l -> Show Permissions and Ownership