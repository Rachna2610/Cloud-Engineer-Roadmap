# Networking Day 07 - Practical
# Topic: Subnetting Fundamentals

## Objective

Learn how to:
- View IP Address
- View Routing Table
- Install ipcalc
- Calculate Network Information
- View Network Interfaces

---

# Step 1 - Create Practical Folder

```bash
mkdir ~/networking-day7-lab
cd ~/networking-day7-lab
```

---

# Step 2 - View IP Address

```bash
ip addr show
```

Observed:

- Interface: eth0
- IP Address: 172.29.13.147/20

---

# Step 3 - Display Only IP Address

```bash
hostname -I
```

Output:

```
172.29.13.147
```

---

# Step 4 - View Routing Table

```bash
ip route
```

Output:

```
default via 172.29.0.1 dev eth0
172.29.0.0/20 dev eth0 proto kernel scope link src 172.29.13.147
```

Understanding:

- Default Gateway: 172.29.0.1
- Network: 172.29.0.0/20

---

# Step 5 - Install ipcalc

```bash
sudo apt update
sudo apt install ipcalc
```

Verify:

```bash
ipcalc --version
```

---

# Step 6 - Calculate Network Information

```bash
ipcalc 172.29.13.147/20
```

This displays:

- IP Address
- Netmask
- Network Address
- Broadcast Address
- Host Range
- Number of Hosts

---

# Step 7 - View Network Interfaces

```bash
ip link show
```

Observed:

- Loopback Interface (lo)
- Ethernet Interface (eth0)

---

# Commands Practiced

```bash
ip addr show
hostname -I
ip route
sudo apt update
sudo apt install ipcalc
ipcalc 172.29.13.147/20
ip link show
```

---

# Practical Learning

During this practical, I learned:

- How to check my IP address
- How to identify my network interface
- How to view the routing table
- How to identify the default gateway
- How to calculate network information using ipcalc
- How to identify the Network ID
- How to identify the Broadcast Address
- How CIDR notation works

---

# Conclusion

This practical helped me understand how subnetting works in a real system by identifying my own IP address, subnet, gateway, and network information. These concepts are essential for cloud networking and AWS VPC configuration.