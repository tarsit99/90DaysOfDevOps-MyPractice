# Core Components of Linux
1. Kernel
- Heart or core of the OS that talks directly to hardware
- Handles CPU, memory, processes, and files
- Acts as a bridge between hardware and applications

2. User space
- Place where users & applications run (e.g., browser, DB, editors)
- Uses system calls to request resources from the kernel
- Keeps programs isolated to avoid system crashes

3. Init / systemd
- First process started (PID 1)
- Starts and manages all system services and handles process like systemctl, journalctl.
- Controls system state after boot

# How Processes Are Created and Managed
- A process = running program
- Created when we run a command
Flow: Shell → Kernel → fork() creates process → exec() loads program

Each process has:
PID (unique ID), Parent process, CPU & memory usage

# Process States
1. Running (R) → Using CPU
2. Sleeping (S) → Waiting for input/resource
3. Stopped (T) → Paused manually (e.g., via signal).
4. Zombie (Z) → Process finished but not cleaned by parent
5. Idle (I) → No active work

# What systemd Does and Why It Matters
- systemd is the first process that runs when computer turn on.
- Manages services (start/stop/restart)
- Manages backgroung services (daemons)
- Automatically restarts failed services
- Manages system calls via systemctl
- Keeps logs via journald
- Uses units for service control

It matters because:
- It provides consistent, simple interface to start, stop, enable, and monitor services (using systemd units).
- Centralized logging
- Managing services easily

# 5 Linux Commands Used Daily
1. ps -ef → View running processes
2. top / htop → Real-time dynamic monitoring for CPU & memory usage
3. systemctl status <service> → Check service status
4. journalctl -u <service> → View service logs
5. kill <PID> → Stop a process ==> SIGKILL