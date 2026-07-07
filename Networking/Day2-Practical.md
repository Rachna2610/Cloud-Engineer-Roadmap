# Day 2 Practical - OSI Model

## Objective

Understand the OSI Model by performing basic networking tasks related to HTTP communication, DNS resolution, and routing.

---

## Commands Practiced

### Check Curl Version

```bash
curl --version
```

Displays the installed version of Curl.

---

### Send HTTP Request

```bash
curl https://example.com
```

Sends an HTTP request and displays the webpage source.

OSI Layer:
- Application Layer

---

### View HTTP Headers

```bash
curl -I https://google.com
```

Displays only the HTTP response headers.

OSI Layer:
- Application Layer

---

### Trace Packet Route

```bash
traceroute google.com
```

Shows the path packets follow to reach the destination.

OSI Layer:
- Network Layer

---

### Resolve Domain Name

```bash
getent hosts google.com
```

Resolves a domain name into its IP address using DNS.

OSI Layer:
- Application Layer

---

## Outcome

- Sent HTTP requests using Curl.
- Viewed HTTP response headers.
- Traced the route to a remote server.
- Resolved domain names using DNS.
- Connected practical Linux commands with different OSI layers.