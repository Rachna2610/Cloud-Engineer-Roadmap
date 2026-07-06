# Day 1 - Networking Fundamentals

## Objective

Learn the basic concepts of networking, understand why networking is important for Cloud Engineers, and become familiar with different network types, topologies, and networking devices.

---

# What is Networking?

Networking is the process of connecting two or more computers or devices so they can communicate and share data or resources.

Examples:
- Sending messages on WhatsApp
- Browsing Google
- Watching YouTube
- Connecting to an AWS EC2 instance
- Accessing files from another computer

Without networking, devices cannot communicate with each other.

---

# Why is Networking Important?

Networking is one of the most important skills for a Cloud Engineer because every cloud service communicates through a network.

Examples:
- Accessing an EC2 instance using SSH
- Connecting an application to a database
- Uploading files to Amazon S3
- Communicating between Kubernetes Pods
- Load Balancing web traffic

A Cloud Engineer must understand how devices communicate before learning cloud platforms like AWS.

---

# Basic Networking Terms

## Network

A network is a collection of connected devices that communicate with each other.

Example:
- Home Wi-Fi
- Office Network
- Internet

---

## Node

Any device connected to a network is called a node.

Examples:
- Laptop
- Desktop
- Mobile Phone
- Printer
- Server
- Router

---

## Host

A host is any device on a network that has its own IP Address and can send or receive data.

Example:
Your laptop connected to Wi-Fi is a host.

---

## Client

A client is a device or application that requests a service from another device.

Examples:
- Web Browser
- Mobile Application

---

## Server

A server is a computer that provides services to clients.

Examples:
- Web Server
- Database Server
- File Server
- Mail Server

Example:

Client (Laptop)
      ↓
Web Server
      ↓
Website Response

---

# Types of Networks

## 1. LAN (Local Area Network)

A LAN connects devices within a small geographical area.

Examples:
- Home Wi-Fi
- School Computer Lab
- Office Network

Advantages:
- Fast
- Secure
- Low Cost

---

## 2. MAN (Metropolitan Area Network)

A MAN connects multiple LANs across a city.

Examples:
- University Campus
- City Government Network

Advantages:
- Covers a city
- Connects multiple buildings

---

## 3. WAN (Wide Area Network)

A WAN connects networks across countries and continents.

Examples:
- Internet
- AWS Global Network
- Company Branches

Advantages:
- Covers large distances
- Connects multiple cities and countries

---

# Network Topologies

A topology describes how devices are connected in a network.

## Star Topology

```
      Switch
     /  |  \
   PC  PC  PC
```

Advantages:
- Easy to manage
- Easy to troubleshoot
- Most commonly used

Disadvantages:
- Switch failure affects the network.

---

## Bus Topology

```
PC ---- PC ---- PC ---- PC
```

Advantages:
- Low cost
- Easy to install

Disadvantages:
- Cable failure affects the whole network.

---

## Ring Topology

```
PC ---- PC
|        |
PC ---- PC
```

Advantages:
- Organized communication

Disadvantages:
- One broken connection can stop communication.

---

## Mesh Topology

```
A------B
|\    /|
| \  / |
|  \/  |
|  /\  |
| /  \ |
|/    \|
C------D
```

Advantages:
- Highly reliable
- Multiple communication paths

Disadvantages:
- Expensive
- Complex

---

# Network Devices

## Hub

A Hub sends incoming data to every connected device.

Characteristics:
- Broadcasts data
- Slow
- Not commonly used today

---

## Switch

A Switch sends data only to the intended device.

Characteristics:
- Uses MAC Addresses
- Faster than Hub
- Most commonly used in LANs

---

## Router

A Router connects different networks.

Functions:
- Connects LAN to Internet
- Routes packets
- Assigns IP Addresses using DHCP

Example:

Home Network
      |
   Router
      |
   Internet

---

## Modem

A Modem connects your network to your Internet Service Provider (ISP).

Without a modem, Internet access is not possible.

---

## Firewall

A Firewall protects a network by allowing or blocking traffic based on predefined security rules.

Example:
- Allow HTTP (Port 80)
- Allow HTTPS (Port 443)
- Block unauthorized traffic

AWS Security Groups act as virtual firewalls.

---

# How Data Travels on the Internet

When you open www.google.com:

Laptop
↓
Wi-Fi
↓
Router
↓
Internet Service Provider (ISP)
↓
Internet
↓
Google Server
↓
Response
↓
Browser

This process happens within milliseconds.

---

# Networking and AWS

AWS networking components are based on real networking concepts.

| Networking Concept | AWS Service |
|--------------------|------------|
| LAN | VPC |
| Router | Route Table |
| Firewall | Security Group |
| Public Network | Internet Gateway |
| Private Network | Private Subnet |
| Load Balancing | Elastic Load Balancer |

Understanding networking makes AWS much easier to learn.

---

# Key Points

- Networking allows devices to communicate.
- Every cloud service depends on networking.
- LAN is used for small areas.
- MAN connects multiple LANs within a city.
- WAN connects networks across countries.
- A Hub broadcasts data to all devices.
- A Switch forwards data only to the correct device.
- A Router connects different networks.
- A Firewall secures a network.
- Networking knowledge is essential for Cloud Engineers.

---

# Interview Questions

1. What is Networking?
2. What is the difference between a Client and a Server?
3. Explain LAN, MAN, and WAN.
4. What is a Router?
5. What is the difference between a Hub and a Switch?
6. What is a Firewall?
7. Why is Networking important in AWS?

---

# Summary

Networking is the backbone of cloud computing. Every AWS service, Docker container, Kubernetes cluster, and web application relies on networking for communication. A strong understanding of networking will make learning AWS, DevOps, and Cloud Engineering much easier.