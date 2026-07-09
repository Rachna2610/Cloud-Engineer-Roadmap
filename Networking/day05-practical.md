# Networking Day 05 - Practical

## Objective

Learn how to inspect network ports, verify HTTP/HTTPS communication, test DNS resolution, and identify active network services.

---

## Commands Performed

### Display Listening TCP Ports

```bash
ss -ltn
```

Displays all listening TCP ports.

---

### Display Listening UDP Ports

```bash
ss -lun
```

Displays all listening UDP ports.

---

### Display Listening Network Services

```bash
ss -tuln
```

Shows all active TCP and UDP listening services.

---

### Test HTTPS Connection

```bash
curl -I https://google.com
```

Retrieves HTTP response headers over HTTPS (Port 443).

---

### Test HTTP Connection

```bash
curl -I http://example.com
```

Retrieves HTTP response headers over HTTP (Port 80).

---

### Resolve Domain Name

```bash
getent hosts google.com
```

Uses DNS to convert a domain name into its IP address.

---

### Check SSH Version

```bash
ssh -V
```

Displays the installed SSH client version.

---

### Display Active Connections

```bash
ss -tun
```

Shows active TCP and UDP connections.

---

## Learning Outcome

- Understood how to inspect network ports.
- Verified HTTP and HTTPS communication.
- Learned how DNS resolves domain names.
- Checked SSH installation.
- Observed active network connections using Linux networking tools.