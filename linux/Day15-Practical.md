# Day 15 Practical – Linux Troubleshooting & System Health

## Objective

Practice basic Linux troubleshooting commands to monitor system health.

## Commands Practiced

### Check system uptime

```bash
uptime
```

### Display running processes

```bash
ps -ef | head
```

### Monitor CPU and memory usage

```bash
top
```

### Check memory usage

```bash
free -h
```

### Check disk usage

```bash
df -h
```

### View recent system logs

```bash
journalctl -n 10
```

### View recent kernel messages

```bash
dmesg | tail
```

## Outcome

- Checked system uptime.
- Monitored running processes.
- Observed CPU and memory usage.
- Verified disk usage.
- Viewed recent system logs.
- Examined kernel messages for troubleshooting.