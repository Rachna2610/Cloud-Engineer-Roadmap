# Day 7 - Linux Networking Fundamentals Practical

## Objective

Learn basic Linux networking commands used by Cloud Engineers to verify network connectivity, DNS resolution, IP addresses, and internet access.

---

## Commands Practiced

### Check Hostname

```bash
hostname
```

Displays the system hostname.

---

### View Network Interfaces

```bash
ip a
```

Displays:

- Network interfaces
- IP addresses
- Network configuration

---

### Check System IP Address

```bash
hostname -I
```

Displays the IP address assigned to the system.

---

### Test Internet Connectivity

```bash
ping google.com
```

Checks whether the system can communicate with Google servers.

Stop the command using:

```text
CTRL + C
```

---

### Test Connectivity to GitHub

```bash
ping github.com
```

Verifies connectivity to GitHub.

---

### Test DNS Resolution

```bash
ping google.com -c 4
```

Checks whether DNS successfully converts the domain name into an IP address.

---

### Use curl Command

```bash
curl google.com
```

Retrieves webpage content from Google.

---

### Check Public IP Address

```bash
curl ifconfig.me
```

or

```bash
curl ifconfig.me/ip
```

Displays the public IP address.

---

### Check wget Version

```bash
wget --version
```

Verifies that wget is installed.

---

### Download a Webpage

```bash
wget https://example.com
```

Downloads webpage content from example.com.

---

### Verify Download

```bash
ls
```

Lists downloaded files.

---

## Commands Saved

```bash
hostname

ip a

hostname -I

ping google.com

ping github.com

ping google.com -c 4

curl google.com

curl ifconfig.me

wget --version

wget https://example.com
```

---

## Learning Outcome

After completing this practical, I learned:

- How to check the system hostname
- How to view network interfaces
- How to find IP addresses
- How to test internet connectivity
- How DNS resolution works
- How to use the ping command
- How to use curl for web requests
- How to use wget for downloading files
- How to check public IP addresses
- Basic networking troubleshooting skills used in AWS EC2 servers

---

## AWS Relevance

These commands are commonly used on AWS EC2 instances to verify:

- Server availability
- Network connectivity
- Internet access
- DNS functionality
- IP configuration

Common AWS commands:

```bash
hostname
ip a
ping google.com
curl ifconfig.me
wget https://example.com
```

These are essential networking skills for Cloud Engineers and DevOps Engineers.