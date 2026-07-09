# Networking Day 05 - Ports & Common Network Protocols

## Objective

Understand what network ports are, why they are required, and learn the most commonly used network protocols and their default port numbers.

---

# 1. What is a Port?

A port is a logical communication endpoint used by applications to send and receive network traffic.

An IP address identifies a device on a network, while a port identifies the specific application or service running on that device.

Example:

IP Address:
192.168.1.10

Port:
80 (HTTP)

When a browser accesses a website, it communicates with the server's IP address on port 80 or 443.

---

# 2. Why Do We Need Ports?

Imagine a computer running multiple services:

- Web Server
- SSH Server
- Database Server
- Mail Server

All these services share the same IP address.

Ports help the operating system deliver incoming traffic to the correct application.

Without ports, the system would not know which application should receive the data.

---

# 3. Port Number Ranges

### Well-Known Ports (0 – 1023)

Reserved for standard services.

Examples:
- HTTP
- HTTPS
- SSH
- FTP
- DNS

---

### Registered Ports (1024 – 49151)

Used by applications and software.

Examples:
- MySQL
- PostgreSQL
- Docker Services

---

### Dynamic / Private Ports (49152 – 65535)

Temporary ports assigned automatically when applications initiate connections.

These are also called Ephemeral Ports.

---

# 4. Common Network Protocols

## HTTP (HyperText Transfer Protocol)

Port: 80

Purpose:
Transfers web pages between browsers and web servers.

Characteristics:
- Not encrypted
- Used for normal websites

Example:
http://example.com

---

## HTTPS (HyperText Transfer Protocol Secure)

Port: 443

Purpose:
Secure communication over the internet.

Characteristics:
- Uses SSL/TLS encryption
- Protects passwords and sensitive data

Example:
https://google.com

---

## SSH (Secure Shell)

Port: 22

Purpose:
Secure remote login to Linux servers.

Example:
ssh user@server-ip

Cloud engineers use SSH almost daily to manage servers.

---

## FTP (File Transfer Protocol)

Port: 21

Purpose:
Transfers files between computers.

Characteristics:
- Not encrypted
- Mostly replaced by SFTP

---

## SFTP (SSH File Transfer Protocol)

Port: 22

Purpose:
Secure file transfer using SSH.

Preferred over FTP because data is encrypted.

---

## DNS (Domain Name System)

Port: 53

Purpose:
Converts domain names into IP addresses.

Example:

google.com
↓

142.250.xxx.xxx

Without DNS, users would have to remember IP addresses.

---

## DHCP (Dynamic Host Configuration Protocol)

Ports:
67 (Server)
68 (Client)

Purpose:
Automatically assigns IP addresses to devices joining a network.

Without DHCP, IP addresses would need to be configured manually.

---

## SMTP (Simple Mail Transfer Protocol)

Port: 25

Purpose:
Sends emails from one mail server to another.

---

## POP3 (Post Office Protocol Version 3)

Port: 110

Purpose:
Downloads emails from a mail server to a local device.

---

## IMAP (Internet Message Access Protocol)

Port: 143

Purpose:
Allows users to read and manage emails directly on the mail server.

Unlike POP3, emails remain on the server.

---

# 5. TCP vs UDP

TCP

- Connection-oriented
- Reliable
- Error checking
- Slower

Examples:
- HTTP
- HTTPS
- SSH
- FTP

---

UDP

- Connectionless
- Faster
- No guaranteed delivery

Examples:
- DNS
- Video Streaming
- Online Games
- Voice Calls

---

# 6. How Communication Happens

Example:

Laptop
↓

HTTPS Request

↓

Port 443

↓

Web Server

↓

Response Returned

The operating system checks the destination port and forwards the request to the correct application.

---

# 7. Importance for Cloud Engineers

Understanding ports is essential because cloud engineers regularly:

- Configure Security Groups
- Manage Firewalls
- Open and Close Ports
- Deploy Web Servers
- Troubleshoot Connectivity
- Configure SSH Access
- Deploy Applications on Cloud Platforms

---

# Common Ports to Remember

| Port | Protocol | Purpose |
|------|----------|---------|
| 20/21 | FTP | File Transfer |
| 22 | SSH / SFTP | Remote Login & Secure File Transfer |
| 25 | SMTP | Send Email |
| 53 | DNS | Domain Name Resolution |
| 67/68 | DHCP | Automatic IP Assignment |
| 80 | HTTP | Web Traffic |
| 110 | POP3 | Receive Email |
| 143 | IMAP | Email Access |
| 443 | HTTPS | Secure Web Traffic |

---

# Interview Questions

### What is a port?

A port is a logical endpoint that allows different applications on the same computer to communicate over a network.

---

### Difference between HTTP and HTTPS?

HTTP transfers data without encryption.

HTTPS encrypts communication using SSL/TLS, making it secure.

---

### Why is SSH preferred over Telnet?

SSH encrypts all communication, while Telnet sends data in plain text.

---

### What is the purpose of DNS?

DNS converts human-readable domain names into IP addresses.

---

### What is the default port of HTTPS?

443

---

# Learning Outcome

After completing Day 05, you will be able to:

- Explain the purpose of network ports.
- Identify common networking protocols.
- Remember important default port numbers.
- Differentiate between TCP and UDP.
- Understand how applications communicate over a network.
- Answer common networking interview questions confidently.