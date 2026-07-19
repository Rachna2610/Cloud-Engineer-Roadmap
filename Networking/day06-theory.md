# Networking Day 06 - Theory
# Topic: TCP vs UDP

## Objective

Learn:
- What is TCP?
- What is UDP?
- Differences between TCP and UDP
- Advantages and Disadvantages
- Real-life Examples
- TCP and UDP in Cloud Computing
- Interview Questions

---

# Introduction

When data is transmitted over the Internet, it follows communication rules known as **Protocols**.

The two most common Transport Layer protocols are:

- TCP (Transmission Control Protocol)
- UDP (User Datagram Protocol)

Both protocols are responsible for transferring data between devices, but they work differently.

---

# What is TCP?

TCP (Transmission Control Protocol) is a **connection-oriented** protocol.

Before sending data, TCP establishes a connection between the sender and the receiver.

It ensures that:

- Data reaches the destination successfully.
- Data is received in the correct order.
- Lost packets are retransmitted.
- Duplicate packets are removed.

TCP focuses on **reliability**.

---

# Features of TCP

- Connection-Oriented
- Reliable Communication
- Error Detection
- Error Recovery
- Ordered Data Delivery
- Flow Control
- Congestion Control

---

# Advantages of TCP

- Reliable data transfer
- Data arrives in order
- Lost packets are retransmitted
- Suitable for important communication
- Error checking and recovery

---

# Disadvantages of TCP

- Slower than UDP
- More overhead
- Requires connection setup
- Higher latency

---

# Applications of TCP

TCP is used where reliable communication is required.

Examples:

- HTTP
- HTTPS
- FTP
- SSH
- Email (SMTP, IMAP, POP3)

---

# What is UDP?

UDP (User Datagram Protocol) is a **connectionless** protocol.

It sends data without establishing a connection.

UDP does not guarantee:

- Delivery
- Order
- Error recovery

Instead, it focuses on **speed**.

---

# Features of UDP

- Connectionless
- Faster communication
- No error recovery
- No packet ordering
- Low overhead

---

# Advantages of UDP

- Very fast
- Low latency
- Minimal overhead
- Suitable for real-time applications

---

# Disadvantages of UDP

- No guarantee of delivery
- No retransmission
- No packet ordering
- Less reliable than TCP

---

# Applications of UDP

UDP is used where speed is more important than reliability.

Examples:

- Video Streaming
- Voice Calls (VoIP)
- Online Gaming
- Live Broadcasting
- DNS Queries

---

# TCP vs UDP

| Feature | TCP | UDP |
|----------|-----|-----|
| Connection | Connection-Oriented | Connectionless |
| Reliability | Reliable | Unreliable |
| Speed | Slower | Faster |
| Packet Ordering | Yes | No |
| Error Recovery | Yes | No |
| Flow Control | Yes | No |
| Congestion Control | Yes | No |
| Overhead | High | Low |

---

# Real-Life Example

## TCP Example

Imagine ordering a laptop online.

The company ensures:

- Correct product
- Correct address
- Safe delivery

If something goes wrong, they send it again.

This is similar to TCP.

---

## UDP Example

Imagine watching a live cricket match.

If one video frame is lost,

the stream continues instead of stopping.

Speed is more important than recovering the lost frame.

This is similar to UDP.

---

# TCP in Cloud Computing

TCP is used for services where reliable communication is required.

Examples:

- Web Servers
- File Transfer
- Database Communication
- Remote Login (SSH)
- API Communication

---

# UDP in Cloud Computing

UDP is used for services where low latency is more important.

Examples:

- Video Streaming
- Voice Communication
- DNS
- Online Gaming
- Live Broadcasting

---

# Key Differences

TCP

- Reliable
- Ordered Delivery
- Connection-Oriented
- Error Recovery
- Slower

UDP

- Fast
- No Connection
- No Error Recovery
- Low Overhead
- Suitable for Real-Time Communication

---

# Interview Questions

## What is TCP?

TCP is a connection-oriented transport layer protocol that provides reliable, ordered, and error-checked communication.

---

## What is UDP?

UDP is a connectionless transport layer protocol that provides fast communication without guaranteeing delivery or order.

---

## Why is TCP slower than UDP?

TCP performs connection establishment, acknowledgments, retransmissions, and error checking, which increases overhead.

---

## When should TCP be used?

Use TCP when reliable communication is required.

Examples:

- HTTP
- HTTPS
- FTP
- SSH
- Email

---

## When should UDP be used?

Use UDP when speed is more important than reliability.

Examples:

- Video Streaming
- Online Gaming
- VoIP
- DNS

---

## Difference Between TCP and UDP

TCP

- Reliable
- Connection-Oriented
- Slower
- Ordered Delivery

UDP

- Faster
- Connectionless
- No Ordering
- No Delivery Guarantee

---

# Summary

Today we learned:

- TCP
- UDP
- Features of TCP
- Features of UDP
- Advantages and Disadvantages
- TCP vs UDP
- Real-life Examples
- Cloud Computing Applications
- Interview Questions