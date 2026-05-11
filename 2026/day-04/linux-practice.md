# Day 04 – Linux Practice: Processes and Services

Today I practiced some basic Linux commands to understand **processes, services, and logs**.

---

# Process Checks

### Command 1
ps aux | head

Purpose:
Shows currently running processes in the system.

Observation:
I could see multiple processes running with their PID, CPU usage, and memory usage.

---

### Command 2
top

Purpose:
Displays real-time process activity and system resource usage.

Observation:
It showed CPU usage, memory usage, and running processes updating live.

---

# Service Checks

### Command 3
systemctl status ssh

Purpose:
Checks the status of the SSH service.

Observation:
The service was active and running successfully.

---

### Command 4
systemctl list-units --type=service

Purpose:
Lists all active services managed by systemd.

Observation:
Many services were running such as ssh, cron, and networking services.

---

# Log Checks

### Command 5
journalctl -u ssh | tail

Purpose:
Shows the recent logs for the SSH service.

Observation:
It displayed login attempts and SSH service activity logs.

---

### Command 6
tail -n 20 /var/log/syslog

Purpose:
Shows the last 20 lines from the system log file.

Observation:
I could see recent system events and background service messages.

---

# Mini Troubleshooting Example

Step 1:
Check if service is running

systemctl status ssh

Step 2:
Check service logs

journalctl -u ssh

Step 3:
Check running processes

ps aux | grep ssh

This basic troubleshooting helps identify if a service is running or facing issues.

---

# What I Learned

- Linux commands help quickly inspect system processes and services.
- systemctl is used to manage and check system services.
- Logs are very important for troubleshooting issues in Linux systems.
