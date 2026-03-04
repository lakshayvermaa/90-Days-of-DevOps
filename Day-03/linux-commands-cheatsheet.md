# Day 03 - Linux Commands Cheat Sheet

Today’s focus was building confidence with essential Linux commands used during real troubleshooting in production environments.

This cheat sheet groups commonly used commands for:

- Process management
- File system operations
- Networking troubleshooting

These commands form a basic toolkit every DevOps engineer uses regularly.

---

# 1. Process Management Commands

| Command | Usage |
|-------|------|
| ps -ef | Show all running processes |
| top | Real-time system resource usage |
| htop | Interactive process viewer |
| kill PID | Terminate a process |
| kill -9 PID | Force kill a process |
| pkill process_name | Kill process by name |
| uptime | Show system uptime and load |
| free -h | Check memory usage |

---

# 2. File System Commands

| Command | Usage |
|-------|------|
| ls -la | List files with detailed info |
| pwd | Show current directory |
| cd directory | Change directory |
| mkdir folder | Create a directory |
| rm file | Remove a file |
| rm -rf folder | Remove directory recursively |
| cp source dest | Copy files |
| mv source dest | Move or rename files |
| df -h | Disk usage of file system |
| du -sh folder | Disk usage of a folder |

---

# 3. Log & System Inspection Commands

| Command | Usage |
|-------|------|
| tail -f file.log | Monitor logs in real-time |
| less file.log | View log files |
| head file | Show first lines of file |
| journalctl -xe | View system logs |
| dmesg | Kernel logs |

---

# 4. Networking Commands

| Command | Usage |
|-------|------|
| ping google.com | Test network connectivity |
| ip addr | Show network interfaces |
| curl url | Test HTTP request |
| dig domain.com | DNS lookup |
| netstat -tulnp | Check open ports |
| ss -tulnp | Show listening services |

---

# Key Takeaway

Real production troubleshooting relies heavily on Linux commands.  
Being comfortable with these commands helps quickly inspect processes, analyze logs, and diagnose network issues.

---

Day 03 completed as part of the **90 Days of DevOps journey**.
