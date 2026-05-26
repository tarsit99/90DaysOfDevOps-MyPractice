# Day 2 – Linux Architecture, Processes, and systemd

## Core Components of Linux
1. Kernel
    * Heart or core of the OS that directly interacts with hardware. It acts as a bridge between hardware and applications.
    * It handles hardware (CPU, memory, processes, and file systems).

2. User space
    * Environment where user applications, libraries and shell run. It interacts with kernel using system calls.
    * It keeps programs or applications isolated to avoid system crashes.

3. Init / systemd
    * First process started by the kernel (PID 1).
    * It is responsible for initializing and managing system services like systemctl, journalctl. It also controls system state after boot.

## How Processes Are Created and Managed
- A process = running program.
- Process is created when we run a command.
Flow: Shell → Kernel → fork() creates process → exec() loads program

In Linux every task is a process and each process is assigned with: PID (unique ID), Parent process, CPU & memory usage.

## Process States
1. Running (R) → Actively using the CPU
2. Sleeping (S) → Waiting for an event/input/resource
3. Stopped (T) → Suspended by a user (via signals)
4. Zombie (Z) → Process execution comepleted but still has a entry in the process table becuase it's parent hasn't acknowledged it.
5. Idle (I) → No active work

## What systemd Does and Why It Matters
systemd is the first process that runs when computer turn-on. It is both service manager and init system. It matters because:
- It manages services using start/stop/restart
- It handles background processes (daemons)
- It automatically restart failed services
- It manages system calls via systemctl
- Provides centralized logging via journald
- Uses units for service control

## 5 Essentials Daily Linux Commands
1. ps aux → List all running processes with user details and resource usage (BSD syntax)
2. top / htop → Dynamic real-time view of CPU & Memory utlization
3. systemctl status <service> → Check service status
4. journalctl -u <service> → View service logs
5. kill <PID> → Terminate a process ==> SIGKILL
6. df -h → Disk space usage in human-readable format.