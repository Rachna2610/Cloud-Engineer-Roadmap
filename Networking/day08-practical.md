# Networking Day 08 - Practical
# Topic: Advanced Subnetting & CIDR

## Objective

Learn how CIDR notation changes subnet size and the number of usable hosts.

---

# Step 1 - Create Practical Folder

```bash
mkdir ~/networking-day8-lab
cd ~/networking-day8-lab
```

---

# Step 2 - Check Current IP Address

```bash
hostname -I
```

Observed Output:

172.29.13.147

---

# Step 3 - View Routing Table

```bash
ip route
```

Observed:

- Default Gateway: 172.29.0.1
- Network: 172.29.0.0/20

---

# Step 4 - Calculate /24 Network

```bash
ipcalc 192.168.1.10/24
```

Observed:

- Network Address
- Broadcast Address
- Host Range
- 254 Usable Hosts

---

# Step 5 - Calculate /25 Network

```bash
ipcalc 192.168.1.10/25
```

Observed:

- Broadcast Address changed
- Host Range changed
- 126 Usable Hosts

---

# Step 6 - Calculate /26 Network

```bash
ipcalc 192.168.1.10/26
```

Observed:

- Smaller subnet
- 62 Usable Hosts

---

# Step 7 - Calculate /27 Network

```bash
ipcalc 192.168.1.10/27
```

Observed:

- Smaller subnet
- 30 Usable Hosts

---

# Step 8 - Calculate /28 Network

```bash
ipcalc 192.168.1.10/28
```

Observed:

- Smaller subnet
- 14 Usable Hosts

---

# Step 9 - View Network Interface

```bash
ip addr show
```

Observed:

- Interface: eth0
- IP Address: 172.29.13.147/20
- Broadcast Address: 172.29.15.255

---

# Commands Practiced

```bash
mkdir ~/networking-day8-lab
cd ~/networking-day8-lab

hostname -I

ip route

ipcalc 192.168.1.10/24

ipcalc 192.168.1.10/25

ipcalc 192.168.1.10/26

ipcalc 192.168.1.10/27

ipcalc 192.168.1.10/28

ip addr show
```

---

# Practical Learning

During this practical, I learned:

- How CIDR affects subnet size.
- How the number of usable hosts changes.
- How Broadcast Address changes.
- How Network Address changes.
- How to use ipcalc for subnet calculations.
- How AWS uses CIDR for VPCs and Subnets.

---

# Conclusion

This practical demonstrated how different CIDR values create different subnet sizes. As the CIDR value increases, the number of available hosts decreases. Understanding CIDR is essential for designing cloud networks, AWS VPCs, and enterprise networks.