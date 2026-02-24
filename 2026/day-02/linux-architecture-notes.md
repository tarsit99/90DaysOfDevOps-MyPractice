# Core Components of Linux
1. Kernel
- Heart or core part of Linux OS
- It directly interacts with hardware like CPU, memory and disks.
- Manages: Process management, File management, User management, Memory management etc.

2. User space
- Place where apps and users operates.
- Ex: web servers, database, editors etc.
- Programs request resources from the kernel using system calls.
- User space keeps user programs isolated to avoid system crashes.

3. Init / systemd
- First process started by the Kernel (PID = 1)
- It is responsible for managing system services during boot and handles others process like systemctl, journalctl.

# How Processes Are Created and Managed
- A process is a running instance of a program.
- When a command is executed: Shell sends a request to the kernel. Kernel creates a new process using fork(). Progeam is loaded into memory using exec().
- Each process has: PID, Parent process, Memory and CPU allocation.

# Process States
1. Running (R) → Process is actively using CPU.
2. Sleeping (S) → Waiting for an event or resource.
3. Stopped (T) → Paused manually (e.g., via signal).
4. Zombie (Z) → Process finished but parent has not collected status.
5. Idle (I) → Waiting state with no immediate work.

# What systemd Does and Why It Matters
- systemd is the first process that runs when computer turn on.
- Manages backgroung services (daemons).
- Restart failed services automatically.
- Manages system calls via systemctl
- Maintains logs via journald

It matters because:
- It provides consistent, simple interface to start, stop, enable, and monitor services (using systemd units).
- Provides Centralized Logging
- Simplifies service lifecycle management

# 5 Linux Commands Used Daily
1. ps -ef → View running processes
2. top / htop → Real-time dynamic monitoring for CPU and memory usage
3. systemctl status <service> → Check service status
4. journalctl -u <service> → View service logs
5. kill <PID> → Stop a process ==> SIGKILL