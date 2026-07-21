# Networking Day 08 - Theory
# Topic: Advanced Subnetting & CIDR

## Objective

Learn:
- What is CIDR?
- Why is CIDR used?
- CIDR Notation
- Borrowing Bits
- Subnets and Hosts
- CIDR in AWS
- Interview Questions

---

# Introduction

In Day 07, we learned what subnetting is.

Today, we will learn how subnetting is represented using **CIDR notation** and how changing the CIDR value affects the number of networks and hosts.

CIDR is used in almost every modern network and cloud platform, including AWS, Azure, and Google Cloud.

---

# What is CIDR?

CIDR stands for **Classless Inter-Domain Routing**.

It is a short and modern way of representing a subnet mask.

Instead of writing:

255.255.255.0

we write:

/24

Example:

IP Address:

192.168.1.10/24

This means:

- First 24 bits represent the Network.
- Remaining 8 bits represent the Host.

---

# Why is CIDR Used?

CIDR is used because it:

- Simplifies subnet representation.
- Uses IP addresses efficiently.
- Supports flexible subnetting.
- Is easier to read and manage.
- Is the standard method used in cloud computing.

---

# CIDR Notation

Some common CIDR values:

| CIDR | Subnet Mask |
|------|----------------|
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |

As the CIDR value increases, the subnet becomes smaller.

---

# Borrowing Bits

Subnetting works by borrowing bits from the Host portion of an IP address.

Original:

Network | Host

After Borrowing:

Network | Borrowed Bits | Host

Borrowing bits creates more subnets but reduces the number of hosts available in each subnet.

---

# Relationship Between CIDR and Hosts

Increasing the CIDR value reduces the number of usable hosts.

Example:

| CIDR | Usable Hosts |
|------|-------------:|
| /24 | 254 |
| /25 | 126 |
| /26 | 62 |
| /27 | 30 |
| /28 | 14 |

Rule:

Higher CIDR → Smaller Subnet → Fewer Hosts

Lower CIDR → Larger Subnet → More Hosts

---

# CIDR in AWS

AWS uses CIDR to create Virtual Private Clouds (VPCs) and Subnets.

Example:

VPC

10.0.0.0/16

Inside the VPC:

Public Subnet

10.0.1.0/24

Private Subnet

10.0.2.0/24

Database Subnet

10.0.3.0/24

This allows AWS to organize resources securely.

---

# Advantages of CIDR

- Better IP Address Utilization
- Supports Flexible Network Design
- Reduces Wasted IP Addresses
- Improves Routing Efficiency
- Essential for Cloud Networking

---

# Key Points

- CIDR is the short form of a subnet mask.
- /24 means the first 24 bits are used for the network.
- Increasing CIDR reduces the number of hosts.
- Borrowing bits creates more subnets.
- CIDR is used in AWS VPCs and Subnets.

---

# Interview Questions

## What is CIDR?

CIDR (Classless Inter-Domain Routing) is a notation used to represent the network portion of an IP address using a prefix length such as /24 instead of a subnet mask.

---

## Why is CIDR used?

CIDR simplifies subnetting, improves IP address utilization, and supports flexible network design.

---

## What does /24 mean?

The first 24 bits are used for the Network, and the remaining 8 bits are used for Hosts.

---

## What happens when the CIDR value increases?

The number of available hosts decreases, and more subnets can be created.

---

## Where is CIDR used?

- AWS
- Azure
- Google Cloud
- Enterprise Networks
- Internet Routing

---

# Summary

Today we learned:

- CIDR
- CIDR Notation
- Borrowing Bits
- Hosts vs Subnets
- AWS CIDR Usage
- Interview Questions