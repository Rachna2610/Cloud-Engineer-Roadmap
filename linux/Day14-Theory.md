# Day 14 – Networking Basics in Linux

## Learning Objectives

After completing this topic, you will be able to:

- Understand computer networking fundamentals.
- Learn about IP addresses.
- Understand DNS and Gateway.
- Learn common Linux networking commands.
- Troubleshoot network connectivity.
- Understand networking concepts used in cloud environments.

---

# What is Networking?

Networking is the process of connecting two or more computers so they can communicate and share resources.

Examples of shared resources:

- Files
- Internet connection
- Printers
- Databases
- Applications

Without networking, computers cannot communicate with each other.

---

# Why is Networking Important?

Networking is essential because it allows:

- Communication between servers
- Internet access
- Cloud services
- Remote management
- Data transfer

Every Cloud Engineer works with networking daily.

---

# What is an IP Address?

An IP (Internet Protocol) Address is a unique address assigned to every device on a network.

Example:

```
192.168.1.10
```

Just like every house has a unique address, every device on a network has a unique IP address.

---

# Types of IP Addresses

## Private IP

Used inside private networks.

Examples:

```
192.168.x.x
10.x.x.x
172.16.x.x – 172.31.x.x
```

Private IPs are not accessible directly from the internet.

---

## Public IP

A Public IP is assigned by an Internet Service Provider (ISP).

It allows devices to communicate over the internet.

Example:

```
34.120.15.10
```

---

# What is DNS?

DNS (Domain Name System) converts domain names into IP addresses.

Example:

```
google.com
```

is translated to an IP address like:

```
142.250.183.14
```

Without DNS, users would need to remember IP addresses instead of website names.

---

# What is a Gateway?

A Gateway connects one network to another.

It acts as the exit point from your local network to the internet.

---

# Important Networking Commands

## Display IP Address

```bash
ip addr
```

Shows:

- IP address
- Network interfaces
- Network configuration

---

## Display Network Interfaces

```bash
ip link
```

Shows all available network interfaces.

---

## Check Connectivity

```bash
ping google.com
```

Purpose:

- Test internet connectivity.
- Check whether another system is reachable.

---

## Display Routing Table

```bash
ip route
```

Shows:

- Default gateway
- Routing information

---

## Display Hostname

```bash
hostname
```

Displays the system's hostname.

---

## Display DNS Information

```bash
cat /etc/resolv.conf
```

Shows configured DNS servers.

---

# Network Troubleshooting

Common steps:

1. Check IP address.

```bash
ip addr
```

2. Check internet connectivity.

```bash
ping google.com
```

3. Check routing table.

```bash
ip route
```

4. Check DNS configuration.

```bash
cat /etc/resolv.conf
```

---

# AWS Cloud Engineer Example

Suppose an EC2 instance cannot access the internet.

A Cloud Engineer checks:

- Instance IP address
- Security Groups
- Route Table
- Internet Gateway
- DNS configuration

Networking knowledge is essential for solving such issues.

---

# Best Practices

- Use static IPs only when required.
- Keep DNS properly configured.
- Monitor network connectivity regularly.
- Secure network access with firewalls.
- Troubleshoot systematically.

---

# Important Commands Summary

```bash
ip addr

ip link

ip route

ping google.com

hostname

cat /etc/resolv.conf
```

---

# Interview Questions

### 1. What is networking?

Networking is the process of connecting computers so they can communicate and share resources.

---

### 2. What is an IP address?

An IP address is a unique identifier assigned to a device on a network.

---

### 3. What is DNS?

DNS (Domain Name System) converts domain names into IP addresses.

---

### 4. Which command displays the IP address?

```bash
ip addr
```

---

### 5. Which command checks internet connectivity?

```bash
ping google.com
```

---

### 6. What is a gateway?

A gateway connects one network to another and provides access to external networks.

---

### 7. Which command displays the routing table?

```bash
ip route
```

---

### 8. Why is networking important for Cloud Engineers?

Networking enables communication between cloud resources, internet access, secure connections, and troubleshooting of cloud infrastructure.

---

# Day 14 Summary

After completing Day 14, you should be able to:

- Understand networking basics.
- Differentiate between private and public IP addresses.
- Understand DNS and gateways.
- Use common Linux networking commands.
- Troubleshoot basic network connectivity issues.
- Apply networking concepts in cloud environments like AWS.