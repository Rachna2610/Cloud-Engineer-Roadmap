# Day 03 - TCP/IP Model

## Objective

Understand the TCP/IP Model, its four layers, and the difference between TCP and UDP protocols.

---

## What is the TCP/IP Model?

The TCP/IP (Transmission Control Protocol/Internet Protocol) Model is the communication model used by the Internet. It defines how data is transmitted between devices over a network.

Unlike the OSI Model, the TCP/IP Model is implemented in real-world networking.

---

## Layers of the TCP/IP Model

### 1. Application Layer

Provides services directly to users and applications.

Protocols:
- HTTP
- HTTPS
- FTP
- DNS
- SMTP
- SSH

---

### 2. Transport Layer

Provides end-to-end communication between devices.

Responsibilities:
- Reliable communication
- Error detection
- Flow control
- Data segmentation

Protocols:
- TCP
- UDP

---

### 3. Internet Layer

Responsible for logical addressing and routing.

Functions:
- IP Addressing
- Packet Routing
- Packet Forwarding

Protocol:
- IP

---

### 4. Network Access Layer

Responsible for transmitting data over the physical network.

Functions:
- MAC Addressing
- Frame Transmission
- Physical Communication

Devices:
- Switch
- Hub
- Network Interface Card (NIC)

---

## TCP vs UDP

| TCP | UDP |
|------|-----|
| Connection-Oriented | Connectionless |
| Reliable | Fast |
| Error Checking | No Error Checking |
| Ordered Delivery | Unordered Delivery |
| Acknowledgement | No Acknowledgement |

---

## TCP Three-Way Handshake

1. SYN
2. SYN-ACK
3. ACK

This process establishes a reliable connection before data transfer begins.

---

## OSI vs TCP/IP

| OSI Model | TCP/IP Model |
|------------|--------------|
| 7 Layers | 4 Layers |
| Conceptual Model | Practical Model |
| Used for Learning | Used on the Internet |

---

## Key Points

- TCP/IP is the networking model used by the Internet.
- It consists of four layers.
- TCP provides reliable communication.
- UDP provides faster communication with lower overhead.
- Cloud platforms such as AWS use the TCP/IP Model.

---

## Outcome

Learned the TCP/IP Model, understood its layers, and compared TCP with UDP communication.