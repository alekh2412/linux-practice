# Day 05 – Linux Troubleshooting Runbook

Today I practiced a basic Linux troubleshooting drill by inspecting the **SSH service** and checking system health.

---

# Target Service / Process

Service inspected: ssh

Command used:
systemctl status ssh

Observation:
The SSH service was active and running. No recent failures were reported.

---

# Environment Information

### Command 1
uname -a

Purpose:
Shows kernel and system architecture details.

Observation:
The system is running a Linux kernel with x86_64 architecture.

---

### Command 2
cat /etc/os-release

Purpose:
Shows the Linux distribution and version.

Observation:
The system is running Ubuntu Linux.

---

# Filesystem Sanity Check

### Command 3
mkdir /tmp/runbook-demo

Purpose:
Creates a temporary directory for testing.

Observation:
Directory was created successfully.

---

### Command 4
cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo

Purpose:
Copies a file and verifies the contents of the directory.

Observation:
File copied successfully and permissions were visible.

---

# CPU and Memory Snapshot

### Command 5
top

Purpose:
Displays real-time CPU and memory usage.

Observation:
CPU usage was low and the system had enough free memory.

---

### Command 6
free -h

Purpose:
Displays memory usage in human-readable format.

Observation:
Most memory was free and no memory pressure was observed.

---

# Disk and I/O Snapshot

### Command 7
df -h

Purpose:
Shows disk usage for all mounted filesystems.

Observation:
Root partition had enough free space.

---

### Command 8
du -sh /var/log

Purpose:
Checks the size of log directory.

Observation:
Log directory size was normal and not consuming too much disk space.

---

# Network Snapshot

### Command 9
ss -tulpn

Purpose:
Lists listening ports and services.

Observation:
SSH was listening on port 22.

---

### Command 10
curl -I https://google.com

Purpose:
Tests HTTP connectivity.

Observation:
Received HTTP response successfully, indicating internet connectivity.

---

# Logs Reviewed

### Command 11
journalctl -u ssh -n 50

Purpose:
Displays the last 50 logs of the SSH service.

Observation:
Logs showed normal SSH login activity with no errors.

---

### Command 12
tail -n 50 /var/log/syslog

Purpose:
Displays the last 50 lines of system logs.

Observation:
System logs showed normal system events.

---

# Quick Findings

- System CPU and memory usage were stable.
- Disk space was sufficient.
- SSH service was running and listening on port 22.
- No critical errors found in recent logs.

---

# If This Worsens (Next Steps)

1. Restart the SSH service  
systemctl restart ssh

2. Check detailed logs for errors  
journalctl -u ssh -xe

3. Investigate process activity  
ps aux | grep ssh
