# Networking Day 06 - Practical
## Topic: TCP vs UDP

### 🎯 Objective

In this practical, we will learn how to:
- View TCP connections
- View UDP connections
- Understand listening ports
- Use the `ss` command
- Test TCP and UDP communication using Netcat (`nc`)
- Compare TCP and UDP practically

---

# Step 1: Create Practical Folder

```bash
mkdir ~/networking-day6-lab
cd ~/networking-day6-lab
```

---

# Step 2: Check TCP Listening Ports

```bash
ss -tln
```

### Explanation

- `-t` → Display TCP sockets
- `-l` → Show listening sockets
- `-n` → Display port numbers instead of service names

---

# Step 3: Check UDP Listening Ports

```bash
ss -uln
```

### Explanation

- `-u` → Display UDP sockets
- `-l` → Show listening sockets
- `-n` → Display numeric port numbers

---

# Step 4: View Active TCP Connections

```bash
ss -t
```

Observe any active TCP connections.

---

# Step 5: View Active UDP Connections

```bash
ss -u
```

Observe any active UDP sockets.

---

# Step 6: Install Netcat

```bash
sudo apt update
sudo apt install netcat-openbsd
```

Verify installation:

```bash
nc -h
```

---

# Step 7: Create a TCP Server

Open **Terminal 1**

```bash
nc -l 5000
```

This command starts a TCP server listening on port **5000**.

---

# Step 8: Connect to the TCP Server

Open **Terminal 2**

```bash
nc localhost 5000
```

Type any message.

Example:

```
Hello TCP
```

Press Enter.

The message should appear in Terminal 1.

---

# Step 9: Create a UDP Server

Open **Terminal 1**

```bash
nc -u -l 5001
```

---

# Step 10: Connect Using UDP

Open **Terminal 2**

```bash
nc -u localhost 5001
```

Type:

```
Hello UDP
```

Press Enter.

Observe the communication.

---

# Step 11: Verify Listening Ports

```bash
ss -tuln
```

Check that:

- TCP Port 5000 is listening
- UDP Port 5001 is listening

---

# Commands Practiced

```bash
ss -tln
ss -uln
ss -t
ss -u
sudo apt update
sudo apt install netcat-openbsd
nc -h
nc -l 5000
nc localhost 5000
nc -u -l 5001
nc -u localhost 5001
ss -tuln
```

---

# Conclusion

In this practical, I learned:

- How to view TCP sockets.
- How to view UDP sockets.
- How to identify listening ports.
- How to create a TCP server using Netcat.
- How to communicate over TCP.
- How to create a UDP server using Netcat.
- How to communicate over UDP.
- The practical differences between TCP and UDP.