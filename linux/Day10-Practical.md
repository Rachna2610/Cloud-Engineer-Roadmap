# Day 10 Practical - Log Management & Monitoring

## Objective

Learn how to:

- View Linux log files
- Monitor logs in real time
- View systemd logs
- Check kernel messages
- Monitor memory, disk, and CPU usage

---

## Commands Used

```bash
ls /var/log

tail /var/log/syslog

tail -f /var/log/syslog

journalctl -n 20

journalctl -u cron

dmesg | tail

free -h

df -h

du -sh .

top
```

---

## What I Learned

### Log Directory

Viewed the Linux log directory:

```bash
ls /var/log
```

---

### View System Log

Viewed the last entries in the system log:

```bash
tail /var/log/syslog
```

---

### Real-Time Log Monitoring

Monitored logs as they were generated:

```bash
tail -f /var/log/syslog
```

Stopped monitoring using:

```text
Ctrl + C
```

---

### View Systemd Logs

Viewed recent system logs:

```bash
journalctl -n 20
```

Viewed logs for the cron service:

```bash
journalctl -u cron
```

---

### Kernel Messages

Viewed recent kernel messages:

```bash
dmesg | tail
```

---

### Memory Usage

Checked RAM usage:

```bash
free -h
```

---

### Disk Usage

Checked available disk space:

```bash
df -h
```

---

### Directory Size

Checked the size of the current directory:

```bash
du -sh .
```

---

### CPU & Process Monitoring

Monitored system resources:

```bash
top
```

Exited using:

```text
q
```

---

## Outcome

Successfully learned how to:

- Locate Linux log files
- Read system logs
- Monitor logs in real time
- Use journalctl
- View kernel messages
- Check memory usage
- Check disk usage
- Monitor CPU and running processes

These skills are essential for Linux Administration, AWS EC2 troubleshooting, DevOps, and Cloud Engineering.