# Networking Day 4 - Practical

## Objective
Learn how to troubleshoot network connectivity, verify DNS configuration, inspect routing information, and analyze network interfaces using Linux networking commands.

## Commands Performed

### 1. Display Network Interface Statistics
```bash
ip -s link
```
Shows packet statistics, errors, dropped packets, and traffic for each network interface.

### 2. Test Connectivity to Google DNS
```bash
ping -c 5 8.8.8.8
```
Verifies internet connectivity using Google's public DNS server.

### 3. Test DNS Name Resolution
```bash
ping -c 5 google.com
```
Checks whether the system can resolve domain names into IP addresses.

### 4. Display Listening Network Ports
```bash
ss -tuln
```
Lists active TCP and UDP listening ports.

### 5. View Routing Table
```bash
ip route
```
Displays routing information and the default gateway.

### 6. Display Neighbor (ARP) Table
```bash
ip neigh
```
Shows nearby devices and MAC address mappings.

### 7. View DNS Configuration
```bash
cat /etc/resolv.conf
```
Displays the DNS servers configured on the system.

### 8. Fetch HTTP Response Headers
```bash
curl -I https://example.com
```
Retrieves only the HTTP response headers from a website.

---

## Learning Outcome

- Understood how to troubleshoot network connectivity.
- Learned to verify DNS resolution and routing.
- Practiced checking interface statistics and listening ports.
- Gained experience using Linux networking diagnostic tools.