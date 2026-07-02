# Day 5 - Process Management in Linux

## Introduction

Every program running in Linux becomes a process.

Examples:

- Chrome
- VS Code
- Docker
- Nginx
- Jenkins
- Python Scripts

As a Cloud Engineer, it is important to know:

- Which processes are running
- How much CPU they use
- How much memory they use
- How to stop unwanted processes
- How to monitor servers

Process management is a daily task on AWS EC2 servers.

---

# What is a Process?

A process is a program currently running in memory.

Example:

```bash
firefox
```

When the command runs, Linux creates a process.

---

# Program vs Process

## Program

- Stored on disk
- Not running

Example:

```text
Google Chrome installed on system
```

## Process

- Running in memory
- Uses CPU and RAM

Example:

```text
Google Chrome currently open
```

---

# Process Lifecycle

```text
Program
   |
   v
Start
   |
   v
Running Process
   |
   v
Stopped / Completed
```

---

# Process ID (PID)

Every process has a unique number called PID.

PID stands for:

```text
Process ID
```

Examples:

```text
Chrome PID = 1523
VS Code PID = 2201
```

Linux uses PID to identify processes.

---

# ps Command

Displays running processes.

Command:

```bash
ps
```

Example Output:

```text
PID   TTY      TIME      CMD
1234  pts/0    00:00:00  bash
5678  pts/0    00:00:00  ps
```

---

# ps -ef

Displays all running processes.

Command:

```bash
ps -ef
```

Example:

```text
UID      PID   PPID   CMD
root       1      0   systemd
root     200      1   sshd
rachna  1500   1490   bash
```

---

# Meaning of Columns

## UID

User who started the process.

Examples:

```text
root
rachna
```

## PID

Process ID.

Example:

```text
1500
```

## PPID

Parent Process ID.

Example:

```text
bash starts vim
```

Then:

```text
bash = Parent Process
vim = Child Process
```

---

# top Command

Used for real-time monitoring.

Command:

```bash
top
```

Shows:

- CPU Usage
- Memory Usage
- Running Processes
- System Load

---

# Why Cloud Engineers Use top

When a server becomes slow:

```bash
top
```

You can identify:

- High CPU usage
- High memory usage
- Problematic processes

---

# htop

Advanced version of top.

Install:

```bash
sudo apt install htop
```

Run:

```bash
htop
```

Advantages:

- Colorful interface
- Easy navigation
- Better monitoring

---

# Foreground Process

Runs directly on the terminal.

Example:

```bash
ping google.com
```

The terminal becomes busy.

---

# Stop Foreground Process

Press:

```text
CTRL + C
```

This stops the process.

---

# Background Process

Runs behind the terminal.

Example:

```bash
sleep 100 &
```

Output:

```text
[1] 1234
```

Where:

```text
1234 = PID
```

The terminal remains free.

---

# jobs Command

Displays background jobs.

Command:

```bash
jobs
```

Example:

```text
[1]+ Running sleep 100 &
```

---

# kill Command

Stops a running process.

Syntax:

```bash
kill PID
```

Example:

```bash
kill 1234
```

Stops process 1234.

---

# kill -9

Forcefully stops a process.

Example:

```bash
kill -9 1234
```

Used when a normal kill does not work.

---

# Finding Process PID

Using ps:

```bash
ps -ef
```

Using pgrep:

```bash
pgrep process-name
```

Example:

```bash
pgrep nginx
```

Output:

```text
2345
```

---

# Process Monitoring in AWS EC2

When a website becomes slow:

Check running processes:

```bash
ps -ef
```

Monitor resources:

```bash
top
```

Find the problematic process.

Stop it:

```bash
kill PID
```

This is a common Cloud Engineer troubleshooting workflow.

---

# Real AWS Example

Website Not Responding

↓

Check Processes

```bash
ps -ef
```

↓

Monitor System

```bash
top
```

↓

Find Problem Process

↓

Kill Process

```bash
kill PID
```

↓

Website Works Again

---

# Important Commands

```bash
ps
ps -ef
top
htop
jobs
kill PID
kill -9 PID
pgrep process-name
```

---

# Summary

## Process

A running instance of a program.

## PID

Unique Process ID.

## ps

Shows running processes.

## ps -ef

Shows all running processes.

## top

Real-time system monitoring.

## jobs

Displays background jobs.

## kill

Stops a running process.

## kill -9

Forcefully stops a process.

---

# Interview Questions

1. What is a process?
2. What is PID?
3. What is the difference between a program and a process?
4. What does the ps command do?
5. What does ps -ef show?
6. What does top command do?
7. What is a background process?
8. What does jobs command do?
9. What is the difference between kill and kill -9?
10. Why is process management important in AWS EC2?