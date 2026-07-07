# Day 2 - OSI Model

## Objective

Understand the OSI (Open Systems Interconnection) Model, its seven layers, and how data travels from one device to another across a network.

---

## What is the OSI Model?

The OSI Model is a conceptual framework that explains network communication by dividing it into seven layers. Each layer performs a specific task and passes data to the next layer.

---

## OSI Layers

### Layer 7 – Application

- Provides network services to end users.
- Examples: Web Browser, Email Client
- Protocols: HTTP, HTTPS, FTP, DNS, SMTP

---

### Layer 6 – Presentation

- Formats data before transmission.
- Performs encryption, decryption, and compression.

---

### Layer 5 – Session

- Establishes, manages, and terminates communication sessions.

---

### Layer 4 – Transport

- Ensures reliable communication.
- Performs segmentation and error checking.
- Protocols:
  - TCP
  - UDP

---

### Layer 3 – Network

- Determines the best path for data.
- Uses IP addresses.
- Device: Router

---

### Layer 2 – Data Link

- Transfers data within the local network.
- Uses MAC addresses.
- Device: Switch

---

### Layer 1 – Physical

- Transmits raw bits through cables or wireless signals.
- Devices: Hub, Repeater

---

## Data Units

| Layer | Data Unit |
|--------|-----------|
| Application | Data |
| Presentation | Data |
| Session | Data |
| Transport | Segment |
| Network | Packet |
| Data Link | Frame |
| Physical | Bits |

---

## Devices Used

| Layer | Device |
|--------|--------|
| Physical | Hub |
| Data Link | Switch |
| Network | Router |

---

## Key Points

- The OSI Model contains seven layers.
- Data moves from Layer 7 to Layer 1 while sending.
- Data moves from Layer 1 to Layer 7 while receiving.
- The Network Layer uses IP addresses.
- The Data Link Layer uses MAC addresses.
- The Transport Layer uses TCP and UDP.
- The Presentation Layer handles encryption.
- The Application Layer interacts with users.

---

## Outcome

Learned the purpose of each OSI layer and understood how data travels through a network.