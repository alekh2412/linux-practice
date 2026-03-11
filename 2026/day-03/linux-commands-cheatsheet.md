# Day 03 – Linux Commands Cheat Sheet

This cheat sheet contains commonly used Linux commands for **process management, file system operations, and networking troubleshooting**.

---

# Process Management Commands

### ps
Shows running processes in the system.

Example:
ps aux

---

### top
Displays real-time CPU and memory usage by processes.

Example:
top

---

### htop
Interactive process viewer (better version of top).

Example:
htop

---

### kill
Terminates a process using its PID.

Example:
kill 1234

---

### killall
Kills processes by name.

Example:
killall nginx

---

### systemctl status
Checks the status of a system service.

Example:
systemctl status ssh

---

### systemctl start
Starts a service.

Example:
systemctl start nginx

---

### systemctl restart
Restarts a service.

Example:
systemctl restart docker

---

# File System Commands

### ls
Lists files and directories.

Example:
ls -l

---

### pwd
Shows the current working directory.

Example:
pwd

---

### cd
Changes the current directory.

Example:
cd /home/user

---

### mkdir
Creates a new directory.

Example:
mkdir project

---

### rm
Deletes files or directories.

Example:
rm file.txt

---

### cp
Copies files or directories.

Example:
cp file.txt backup.txt

---

### mv
Moves or renames files.

Example:
mv file.txt newfile.txt

---

### chmod
Changes file permissions.

Example:
chmod 755 script.sh

---

### chown
Changes file ownership.

Example:
sudo chown user file.txt

---

### df
Shows disk space usage.

Example:
df -h

---

### du
Shows file or directory size.

Example:
du -sh *

---

# Networking Troubleshooting Commands

### ping
Checks network connectivity to another host.

Example:
ping google.com

---

### ip addr
Displays IP addresses of network interfaces.

Example:
ip addr show

---

### curl
Transfers data from a URL (used to test APIs or websites).

Example:
curl https://example.com

---

### dig
Queries DNS information for a domain.

Example:
dig google.com

---

### netstat
Displays network connections and listening ports.

Example:
netstat -tulpn

---

# Key Takeaways

- Linux commands help you inspect and troubleshoot systems quickly.
- Process commands help monitor and control running applications.
- File system commands manage files, directories, and permissions.
- Networking commands help diagnose connectivity and DNS issues.

These commands form the **basic toolkit for every DevOps engineer**.
