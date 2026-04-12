# Core Components of Linux
1. Kernel
    * Heart or core of the OS that directly interacts with hardware
    * Handles CPU, memory, processes, and file systems
    * Acts as a bridge between hardware and applications

2. User space
    * Place where user application run (e.g., browser, DB, editors)
    * Interacts with kernel using system calls
    * Keeps programs or applications isolated to avoid system crashes

3. Init / systemd
    * First process started (PID 1)
    * Responsible for starting and managing system services like systemctl, journalctl
    * Controls system state after boot

# How Processes Are Created and Managed
- A process = running program
- Created when we run a command
Flow: Shell → Kernel → fork() creates process → exec() loads program

Each process has:
PID (unique ID), Parent process, CPU & memory usage

# Process States
1. Running (R) → Using CPU
2. Sleeping (S) → Waiting for input/resource
3. Stopped (T) → Paused manually (via signal)
4. Zombie (Z) → Process finished but not cleaned by parent
5. Idle (I) → No active work

# What systemd Does and Why It Matters
systemd is the first process that runs when computer turn-on
- Manages services (start/stop/restart)
- Handles background processed (daemons)
- Automatically restarts failed services
- Manages system calls via systemctl
- Provides logging via journald
- Uses units for service control

It matters because:
- Simple and consistent service management (systemctl)
- Centralized logging and faster troubleshooting
- Ensures system reliability through auto-restart and monitoring

# 5 Linux Commands Used Daily
1. ps -ef → View running processes
2. top / htop → Dynamic real-time CPU and Memory monitoring
3. systemctl status <service> → Check service status
4. journalctl -u <service> → View service logs
5. kill <PID> → Stop a process ==> SIGKILL