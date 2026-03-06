# Day 05 - Linux Troubleshooting Runbook

Today I practiced a Linux troubleshooting drill to simulate how a DevOps engineer inspects a system when a service might be misbehaving.

The goal was to capture a quick system health snapshot including:

- CPU usage
- Memory usage
- Disk usage
- Network status
- Service logs

Target service inspected in this drill:

**SSH Service (sshd)**

---

## Environment Information

### System Details

```bash
uname -a
```

Shows kernel version and system architecture.

```bash
cat /etc/os-release
```

Displays Linux distribution information.

---

## Snapshot: CPU & Memory

Check running processes and CPU usage:

```bash
top
```

Observation: CPU usage appears normal with most resources idle.

Check memory usage:

```bash
free -h
```

Observation: System has available memory and no swap pressure detected.

Inspect SSH process:

```bash
ps -ef | grep ssh
```

Observation: SSH service is running normally.

---

## Snapshot: Disk & IO

Check disk usage:

```bash
df -h
```

Observation: Disk usage is within safe limits.

Check log directory size:

```bash
du -sh /var/log
```

Observation: Log files consuming moderate disk space.

---

## Snapshot: Network

Check listening ports and active services:

```bash
ss -tulpn
```

Observation: SSH service listening on port 22.

Test service connectivity:

```bash
curl -I localhost
```

Observation: Service responds correctly.

---

## Logs Reviewed

Check SSH logs:

```bash
journalctl -u ssh -n 50
```

Observation: No recent authentication errors.

Check system logs:

```bash
tail -n 50 /var/log/syslog
```

Observation: System running normally without critical warnings.

---

## Quick Findings

- CPU and memory usage stable
- Disk space within safe limits
- SSH service active and listening on port 22
- No critical errors found in recent logs

System health appears normal.

---

## If This Worsens (Next Steps)

If issues appear later, the following actions would be taken:

Restart the service:

```bash
sudo systemctl restart ssh
```

Increase logging verbosity for deeper troubleshooting.

Trace the process using tools like:

```bash
strace
```

or

```bash
lsof
```

to inspect resource usage or blocked operations.

---

## Key Takeaway

A structured troubleshooting routine helps engineers:

- Capture system health quickly
- Investigate logs before restarting services
- Diagnose production issues confidently

This runbook builds a repeatable troubleshooting workflow for real production incidents.

---

Day 05 completed as part of the **90 Days of DevOps journey**.
