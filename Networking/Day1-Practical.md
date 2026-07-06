# Day 1 Practical - Networking Fundamentals

## Objective

Learn basic Linux networking commands to inspect network configuration.

## Commands Practiced

### Display Hostname

```bash
hostname
```

### Display IP Address

```bash
hostname -I
```

### Display Network Interfaces

```bash
ip addr
```

```bash
ip link
```

### Display Routing Table

```bash
ip route
```

### Display DNS Server

```bash
cat /etc/resolv.conf
```

### Test Internet Connectivity

```bash
ping -c 4 google.com
```

### Display Listening Ports

```bash
ss -tuln
```

## Outcome

- Displayed hostname
- Checked IP address
- Viewed network interfaces
- Viewed routing table
- Checked DNS configuration
- Tested internet connectivity
- Viewed listening ports