 # Day 02 – Linux Architecture, Processes, and systemd

## Linux Architecture

A Linux system mainly consists of three core components:

### 1. Kernel
- The kernel is the core of the Linux operating system.
- It manages communication between hardware and software.
- It controls system resources like CPU, memory, disk, and devices.

### 2. User Space
- User space is where applications and user programs run.
- Examples: bash, nginx, docker, vim.
- User commands interact with the kernel to access hardware resources.

### 3. Init / systemd
- When a Linux system boots, the first process that starts is the init system.
- In most modern Linux systems, **systemd** is used as the init system.
- It manages system services and background processes.

---

## Processes in Linux

A **process** is a running instance of a program.

Examples:
- nginx running
- docker running
- ssh service running

Each process has a unique **PID (Process ID)** which identifies it in the system.

---

## Process States

Common Linux process states include:

- **Running (R)**  
  The process is currently using the CPU.

- **Sleeping (S)**  
  The process is waiting for an event such as input/output.

- **Stopped (T)**  
  The process has been paused or stopped.

- **Zombie (Z)**  
  The process has finished execution but still exists because the parent process has not cleaned it up.

---

## systemd

**systemd** is the service manager used by most modern Linux distributions.

It is responsible for:

- Starting and stopping system services
- Managing background services
- Handling system logs
- Controlling the system boot process

Examples of services managed by systemd:
- ssh
- nginx
- docker

---

## Useful Commands

These commands are commonly used for managing processes and services:

```bash
ps aux          # Shows running processes
top             # Displays real-time process usage
systemctl status ssh     # Check status of SSH service
systemctl restart nginx  # Restart nginx service
journalctl -u ssh        # View logs for SSH service
