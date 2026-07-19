# Networking Day 07 - Theory
# Topic: Subnetting Fundamentals

## Objective

Learn:
- What is Subnetting?
- Why do we need Subnetting?
- Network
- Subnet
- IP Address
- Subnet Mask
- Network ID
- Host ID
- Broadcast Address
- AWS Connection

---

# What is a Network?

A network is a group of interconnected devices that communicate with each other and share resources.

Examples:
- Home Wi-Fi
- Office Network
- College Network

---

# What is an IP Address?

An IP (Internet Protocol) Address is a unique address assigned to every device connected to a network.

Example:

192.168.1.25

It helps devices identify and communicate with each other.

---

# Problem with One Large Network

If hundreds of devices are connected to one network:

- High broadcast traffic
- Slow network performance
- Difficult troubleshooting
- Security issues
- Difficult management

---

# What is Subnetting?

Subnetting is the process of dividing one large network into multiple smaller networks called subnets.

Example:

Company Network

↓

HR Department

↓

Finance Department

↓

IT Department

↓

Sales Department

Each department has its own subnet.

---

# What is a Subnet?

A subnet is a smaller network created from a larger network using subnetting.

Subnet = Small Network

Subnetting = Process of creating subnets

---

# What is a Subnet Mask?

A subnet mask separates the Network Portion and the Host Portion of an IP address.

Example:

IP Address

192.168.1.25

Subnet Mask

255.255.255.0

Network Portion

192.168.1

Host Portion

25

---

# Network ID

The Network ID identifies the network to which a device belongs.

Example:

IP Address:

192.168.1.25

Subnet Mask:

255.255.255.0

Network ID:

192.168.1.0

---

# Host ID

The Host ID identifies an individual device within a network.

Example:

IP:

192.168.1.25

Host ID:

25

Every device in the network must have a unique Host ID.

---

# Broadcast Address

A Broadcast Address is used to send data to all devices within the same subnet.

Example:

Network:

192.168.1.0/24

Broadcast:

192.168.1.255

The Broadcast Address cannot be assigned to any device.

---

# Benefits of Subnetting

- Reduces network traffic
- Improves performance
- Enhances security
- Simplifies management
- Makes troubleshooting easier
- Efficient use of IP addresses

---

# AWS Connection

Subnetting is one of the most important concepts in AWS.

Inside a VPC, multiple subnets are created.

Example:

VPC

↓

Public Subnet

↓

Private Subnet

↓

Database Subnet

Public Subnet:
- Web Server
- Load Balancer

Private Subnet:
- Application Server

Database Subnet:
- MySQL
- PostgreSQL
- MongoDB

---

# Key Points

- Network = Collection of connected devices
- IP Address = Unique address of a device
- Subnet = Small network
- Subnetting = Dividing a large network
- Subnet Mask = Separates Network and Host portions
- Network ID = Identifies the network
- Host ID = Identifies the device
- Broadcast Address = Sends data to all devices in a subnet
- AWS VPC uses subnetting extensively

---

# Interview Questions

## What is subnetting?

Subnetting is the process of dividing one large network into multiple smaller networks called subnets.

---

## Why do we use subnetting?

- Better performance
- Better security
- Better management
- Reduced broadcast traffic
- Efficient IP utilization

---

## Difference between Subnet and Subnetting

Subnet:
A smaller network.

Subnetting:
The process of creating smaller networks.

---

## What is a Subnet Mask?

A subnet mask separates the network portion and host portion of an IP address.

---

## What is Network ID?

It identifies the network.

---

## What is Host ID?

It identifies a device inside the network.

---

## What is Broadcast Address?

It is used to send data to all devices in a subnet.

---

# Summary

Today we learned:

- Network
- IP Address
- Problems with large networks
- Subnet
- Subnetting
- Subnet Mask
- Network ID
- Host ID
- Broadcast Address
- Benefits of Subnetting
- AWS Connection