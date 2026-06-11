# Day 6 - Services and Systemctl in Linux

## Introduction

Many applications in Linux run as services.

Examples:

- Nginx
- Apache
- Docker
- Jenkins
- SSH
- MySQL

Services are important because they keep running in the background and provide functionality to users and applications.

As a Cloud Engineer, you must know how to:

- Start services
- Stop services
- Restart services
- Check service status
- Enable services at boot

These tasks are commonly performed on AWS EC2 servers.

---

# What is a Service?

A service is a program that runs continuously in the background and performs a specific task.

Examples:

- Web Server
- Database Server
- SSH Server
- Docker Service

Unlike normal applications, services continue running even when users are not actively interacting with them.

---

# Service Example

```text
User
  |
  v
Website
  |
  v
Nginx Service
  |
  v
Linux Server
```

If the Nginx service stops:

```text
Website Becomes Unavailable
```

---

# What is systemd?

Modern Linux distributions use a service manager called:

```text
systemd
```

systemd is responsible for:

- Managing services
- Managing processes
- System startup
- Boot process
- Logging

Think of systemd as the manager of the Linux operating system.

---

# What is systemctl?

The command used to interact with systemd is:

```bash
systemctl
```

systemctl is one of the most important commands for Linux administrators and Cloud Engineers.

---

# Check Service Status

Command:

```bash
systemctl status service-name
```

Example:

```bash
systemctl status ssh
```

Possible Output:

```text
Active: active (running)
```

Meaning:

```text
Service is currently running
```

---

# Start a Service

Command:

```bash
sudo systemctl start service-name
```

Example:

```bash
sudo systemctl start nginx
```

Purpose:

```text
Starts the Nginx service
```

---

# Stop a Service

Command:

```bash
sudo systemctl stop service-name
```

Example:

```bash
sudo systemctl stop nginx
```

Purpose:

```text
Stops the Nginx service
```

---

# Restart a Service

Command:

```bash
sudo systemctl restart service-name
```

Example:

```bash
sudo systemctl restart nginx
```

Purpose:

- Apply configuration changes
- Recover from errors
- Restart the service completely

---

# Reload a Service

Command:

```bash
sudo systemctl reload nginx
```

Purpose:

```text
Apply configuration changes without fully restarting the service
```

---

# Enable Service at Boot

Command:

```bash
sudo systemctl enable service-name
```

Example:

```bash
sudo systemctl enable nginx
```

Purpose:

```text
Automatically start the service whenever Linux boots
```

---

# Disable Service at Boot

Command:

```bash
sudo systemctl disable nginx
```

Purpose:

```text
Prevent the service from starting automatically during boot
```

---

# Check if a Service is Enabled

Command:

```bash
systemctl is-enabled nginx
```

Possible Output:

```text
enabled
```

or

```text
disabled
```

---

# List Running Services

Command:

```bash
systemctl list-units --type=service
```

Displays:

```text
ssh.service
cron.service
docker.service
nginx.service
```

and many other running services.

---

# SSH Service

One of the most important Linux services.

Check Status:

```bash
systemctl status ssh
```

Purpose:

- Remote Login
- Server Administration
- AWS EC2 Access

Without SSH:

```text
Cannot connect to Linux server remotely
```

---

# Docker Service

After installing Docker:

Check Status:

```bash
systemctl status docker
```

Start Docker:

```bash
sudo systemctl start docker
```

Enable Docker at Boot:

```bash
sudo systemctl enable docker
```

---

# Nginx Service

Install:

```bash
sudo apt install nginx
```

Check Status:

```bash
systemctl status nginx
```

Start Service:

```bash
sudo systemctl start nginx
```

Stop Service:

```bash
sudo systemctl stop nginx
```

Restart Service:

```bash
sudo systemctl restart nginx
```

---

# Service States

## Active

```text
Running
```

Example:

```text
Active: active (running)
```

---

## Inactive

```text
Stopped
```

Example:

```text
Active: inactive
```

---

## Failed

```text
Service crashed or encountered an error
```

Example:

```text
Active: failed
```

---

# Real AWS Scenario

Problem:

```text
Website Not Working
```

Step 1:

```bash
systemctl status nginx
```

Output:

```text
inactive
```

Step 2:

```bash
sudo systemctl start nginx
```

Result:

```text
Website Becomes Available Again
```

---

# Real Cloud Engineer Workflow

Launch EC2 Instance

↓

Install Nginx

```bash
sudo apt install nginx
```

↓

Check Service Status

```bash
systemctl status nginx
```

↓

Enable Service

```bash
sudo systemctl enable nginx
```

↓

Website Available

---

# Important Commands

```bash
systemctl status service-name

sudo systemctl start service-name

sudo systemctl stop service-name

sudo systemctl restart service-name

sudo systemctl reload service-name

sudo systemctl enable service-name

sudo systemctl disable service-name

systemctl is-enabled service-name

systemctl list-units --type=service
```

---

# Summary

## Service

A background program that performs a specific task continuously.

## systemd

The service manager of modern Linux systems.

## systemctl

The command used to manage services.

## Start

Starts a service immediately.

## Stop

Stops a running service.

## Restart

Stops and starts a service again.

## Enable

Starts a service automatically during boot.

## Disable

Prevents automatic startup during boot.

---

# Interview Questions

1. What is a service in Linux?
2. What is systemd?
3. What is systemctl?
4. How do you check service status?
5. How do you start a service?
6. How do you stop a service?
7. How do you restart a service?
8. What is the difference between start and enable?
9. Why is SSH important in AWS EC2?
10. Why are services important for Cloud Engineers?