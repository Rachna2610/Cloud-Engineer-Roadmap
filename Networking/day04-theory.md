# Networking Day 4 - Network Troubleshooting & Diagnostic Tools

## Objective
Learn how to troubleshoot network connectivity issues using Linux networking commands. Understand how to verify internet access, DNS resolution, routing, and network interface status.

---

# 1. Network Troubleshooting

Network troubleshooting is the process of identifying and resolving connectivity or communication problems between devices.

Common issues include:
- No internet connection
- DNS resolution failure
- Incorrect IP configuration
- Routing problems
- Network interface failure

Linux provides several built-in commands to diagnose these problems.

---

# 2. Ping

The `ping` command tests connectivity between your system and another device.

Example:
```bash
ping google.com
```

Uses:
- Verify internet connectivity
- Check whether a host is reachable
- Measure network latency

---

# 3. Interface Statistics

The `ip -s link` command displays packet statistics for every network interface.

Example:
```bash
ip -s link
```

It shows:
- Packets sent
- Packets received
- Errors
- Dropped packets

This helps identify network interface issues.

---

# 4. Routing Table

A routing table tells Linux where to send outgoing network packets.

Command:
```bash
ip route
```

Information displayed:
- Default Gateway
- Local Network
- Destination Routes

The default gateway is used whenever the destination network is outside the local network.

---

# 5. ARP / Neighbor Table

Linux stores information about nearby devices in the Neighbor Table.

Command:
```bash
ip neigh
```

It displays:
- IP Address
- MAC Address
- Network Interface

This helps verify communication within the local network.

---

# 6. DNS Configuration

DNS (Domain Name System) converts domain names into IP addresses.

Configuration file:
```bash
cat /etc/resolv.conf
```

It contains:
- DNS Server Address
- Search Domains

If DNS is incorrect, websites may not open even if internet connectivity exists.

---

# 7. Socket Statistics

The `ss` command displays active network connections.

Example:
```bash
ss -tuln
```

It shows:
- Listening Ports
- TCP Connections
- UDP Connections

Useful for checking running network services.

---

# 8. HTTP Header Request

The `curl` command can retrieve data from websites.

Example:
```bash
curl -I https://example.com
```

The `-I` option fetches only the HTTP headers.

This is useful for:
- Checking website availability
- Viewing HTTP response codes
- Verifying server responses

---

# Key Commands

```bash
ip -s link
ping -c 5 8.8.8.8
ping -c 5 google.com
ss -tuln
ip route
ip neigh
cat /etc/resolv.conf
curl -I https://example.com
```

---

# Learning Outcome

After completing Day 4, you will be able to:

- Troubleshoot basic network problems.
- Verify internet and DNS connectivity.
- Analyze routing information.
- Inspect network interface statistics.
- Check listening ports and active connections.
- Understand Linux networking diagnostic tools.