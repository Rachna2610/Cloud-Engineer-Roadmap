# Day 15 – Linux Troubleshooting and Best Practices

## Learning Objectives

After completing this topic, you will be able to:

- Understand Linux troubleshooting.
- Learn a systematic approach to solving problems.
- Identify common Linux issues.
- Use troubleshooting commands.
- Follow best practices for maintaining Linux servers.
- Understand troubleshooting in cloud environments like AWS.

---

# What is Troubleshooting?

Troubleshooting is the process of identifying, analyzing, and resolving problems in a Linux system.

A Linux administrator or Cloud Engineer spends a significant amount of time troubleshooting servers to ensure they remain available and perform efficiently.

---

# Why is Troubleshooting Important?

Servers can experience various issues such as:

- High CPU usage
- Low memory
- Full disk space
- Network failures
- Service failures
- Permission issues

Quick troubleshooting helps minimize downtime and keeps applications running smoothly.

---

# Common Linux Problems

Some common issues include:

- Server is slow
- Disk is full
- Service is not running
- Network is unavailable
- File permission denied
- High memory usage
- High CPU usage

---

# Troubleshooting Steps

A good troubleshooting process follows these steps:

1. Identify the problem.
2. Collect information.
3. Analyze the issue.
4. Apply the solution.
5. Verify the result.
6. Document the solution.

Never make changes without understanding the root cause.

---

# Check System Information

Display system details:

```bash
uname -a
```

Shows:

- Kernel version
- Architecture
- Hostname

---

# Check Running Processes

Display running processes:

```bash
ps -ef
```

or

```bash
top
```

These commands help identify processes consuming excessive CPU or memory.

---

# Check Memory Usage

```bash
free -h
```

Shows:

- Total memory
- Used memory
- Free memory
- Swap memory

---

# Check Disk Usage

```bash
df -h
```

Displays available and used disk space.

---

# Check Directory Size

```bash
du -sh directory_name
```

Helps identify large directories consuming disk space.

---

# Check System Logs

View recent log entries:

```bash
journalctl -n 20
```

System logs often contain useful error messages.

---

# Check Network Connectivity

Test internet connectivity:

```bash
ping google.com
```

If ping fails, investigate:

- Network interface
- Gateway
- DNS
- Firewall

---

# Check Running Services

Display service status:

```bash
systemctl status service_name
```

Example:

```bash
systemctl status cron
```

---

# Useful Troubleshooting Commands

```bash
uname -a

ps -ef

top

free -h

df -h

du -sh

journalctl -n 20

ping google.com

systemctl status service_name
```

---

# Linux Best Practices

- Keep the system updated.
- Monitor CPU, memory, and disk usage regularly.
- Create regular backups.
- Use strong passwords.
- Follow the principle of least privilege.
- Avoid logging in as the root user for daily tasks.
- Remove unnecessary software.
- Monitor logs regularly.
- Restart failed services safely.
- Document important changes.

---

# AWS Cloud Engineer Example

Suppose an EC2 instance becomes unreachable.

A Cloud Engineer checks:

- Is the instance running?
- Is the CPU overloaded?
- Is memory exhausted?
- Is the disk full?
- Are Security Groups configured correctly?
- Is the required service running?
- Are there any errors in the logs?

Following a structured troubleshooting process helps resolve issues quickly.

---

# Interview Questions

### 1. What is troubleshooting?

Troubleshooting is the process of identifying and resolving problems in a computer system.

---

### 2. Which command checks memory usage?

```bash
free -h
```

---

### 3. Which command checks disk usage?

```bash
df -h
```

---

### 4. Which command shows running processes?

```bash
ps -ef
```

or

```bash
top
```

---

### 5. Which command displays recent system logs?

```bash
journalctl -n 20
```

---

### 6. Why are system logs important?

System logs record events and errors, making it easier to diagnose and fix problems.

---

### 7. What should be the first step in troubleshooting?

Identify and clearly understand the problem before making any changes.

---

### 8. Why is troubleshooting an important skill for Cloud Engineers?

Cloud Engineers manage production servers where quick problem diagnosis and resolution are essential to minimize downtime and maintain service availability.

---

# Day 15 Summary

After completing Day 15, you should be able to:

- Understand the Linux troubleshooting process.
- Diagnose common Linux problems.
- Monitor CPU, memory, disk, and services.
- Analyze system logs.
- Apply Linux best practices.
- Troubleshoot Linux systems used in AWS and other cloud environments.