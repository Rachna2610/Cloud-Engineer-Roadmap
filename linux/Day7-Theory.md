# Day 7 - Linux Networking Fundamentals

## Introduction

Networking is the backbone of Cloud Computing. Every AWS service, website, server, and application communicates through networks. As a Cloud Engineer, understanding networking is essential because AWS services such as EC2, VPC, Load Balancers, Route Tables, and Security Groups all depend on networking concepts.

---

# What is Networking?

Networking is the process of connecting two or more devices so that they can communicate and exchange data.

Examples:

- Laptop ↔ Internet
- Mobile ↔ Wi-Fi Router
- EC2 Server ↔ Database Server
- User ↔ Website

Without networking, devices cannot communicate with each other.

---

# What is an IP Address?

IP Address stands for Internet Protocol Address.

An IP address is a unique address assigned to every device connected to a network.

Example:

```text
192.168.1.10
```

Just as every house has a unique address, every device on a network has a unique IP address.

Purpose of IP Address:

- Identifies devices on a network
- Enables communication between devices
- Allows data to reach the correct destination

---

# IPv4 Address

IPv4 is the most commonly used IP version.

Format:

```text
192.168.1.10
```

Characteristics:

- Contains four numbers
- Numbers are separated by dots
- Each number ranges from 0 to 255

Examples:

```text
10.0.0.5
172.16.1.2
192.168.1.100
```

---

# Public IP Address

A Public IP Address is accessible over the Internet.

Example:

```text
13.235.120.50
```

Uses:

- Websites
- Cloud Servers
- Public Applications

Characteristics:

- Unique worldwide
- Reachable from the Internet

---

# Private IP Address

A Private IP Address is used inside private networks.

Examples:

```text
192.168.x.x
10.x.x.x
172.16.x.x
```

Uses:

- Home Networks
- Office Networks
- AWS VPC Internal Communication

Characteristics:

- Not accessible directly from the Internet
- Used for internal communication

---

# Public IP vs Private IP

| Public IP | Private IP |
|------------|------------|
| Accessible from Internet | Accessible only within private network |
| Globally unique | Reusable in different networks |
| Used for public services | Used for internal communication |

---

# What is Hostname?

Hostname is the name assigned to a computer or server.

Examples:

```text
web-server
database-server
ubuntu-server
```

Hostname helps identify systems without remembering IP addresses.

---

# Check Hostname

Command:

```bash
hostname
```

Example Output:

```text
LAPTOP-HRH98GG9
```

---

# What is DNS?

DNS stands for Domain Name System.

DNS converts domain names into IP addresses.

Example:

```text
google.com
```

becomes

```text
142.250.xxx.xxx
```

DNS allows users to access websites using names instead of IP addresses.

---

# DNS Working

```text
google.com
      ↓
DNS Server
      ↓
IP Address
      ↓
Google Server
```

---

# What is Ping?

Ping is used to test network connectivity between systems.

Command:

```bash
ping google.com
```

Purpose:

- Check Internet connectivity
- Verify server availability
- Troubleshoot network issues

Stop Ping:

```text
CTRL + C
```

---

# What is a Network Interface?

A Network Interface is a connection point between a device and a network.

Examples:

- Ethernet
- Wi-Fi
- Virtual Network Adapter

Linux identifies interfaces using names such as:

```text
eth0
ens33
wlan0
```

---

# View Network Interfaces

Command:

```bash
ip a
```

Purpose:

- View network interfaces
- View IP addresses
- Check network configuration

---

# Loopback Interface (lo)

Loopback Interface represents the local machine itself.

IP Address:

```text
127.0.0.1
```

Uses:

- Local testing
- Internal communication

---

# Localhost

Localhost refers to the current machine.

IP Address:

```text
127.0.0.1
```

Examples:

- Testing web applications
- Local development

---

# curl Command

curl is used to communicate with websites and APIs.

Example:

```bash
curl google.com
```

Uses:

- API Testing
- Website Connectivity Testing
- Downloading Content

Cloud Engineers use curl frequently when working with AWS services and APIs.

---

# wget Command

wget is used to download files from the Internet.

Example:

```bash
wget https://example.com/file.zip
```

Uses:

- Downloading Software
- Downloading Scripts
- Downloading Files

---

# Importance in AWS

When working with EC2 instances, Cloud Engineers commonly use:

```bash
hostname
ip a
ping google.com
curl google.com
wget URL
```

These commands help verify:

- Network Connectivity
- Internet Access
- DNS Resolution
- Server Reachability

---

# Important Commands

```bash
hostname

ip a

ping google.com

curl google.com

wget URL
```

---

# Interview Questions

### What is an IP Address?

A unique address assigned to a device on a network.

### What is the difference between Public and Private IP?

Public IP is accessible from the Internet, while Private IP is used only within private networks.

### What is DNS?

A system that converts domain names into IP addresses.

### What is Ping?

A command used to test network connectivity.

### What is Hostname?

The name assigned to a computer or server.

### What is Localhost?

The local machine itself, represented by IP address 127.0.0.1.

### What does `ip a` do?

Displays network interfaces and IP addresses.

### What does `curl` do?

Communicates with websites and APIs.

### What does `wget` do?

Downloads files from the Internet.

---

# Day 7 Summary

- Learned Networking Fundamentals
- Understood IP Addresses
- Learned Public and Private IPs
- Understood DNS
- Learned Hostname
- Learned Ping Command
- Learned Network Interfaces
- Learned curl and wget Commands
- Understood networking concepts used in AWS Cloud Infrastructure