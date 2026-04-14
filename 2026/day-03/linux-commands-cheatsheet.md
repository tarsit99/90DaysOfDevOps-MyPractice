# ⚙️ Process management
- ps -ef → List all running processes
- top → Dynamic real-time CPU/memory usage
- htop → Interactive process viewer, similar to top but allows you to scroll vertically and horizontally, and interact using a pointing device (mouse)
- kill <PID> → Terminate a process
- kill -9 <PID> → Force kill process
- free -m → Check memory usage
- nproc → Show number of CPU cores
- uptime → System load & uptime

# 📁 File system commands
- ls -l → List files in long format
- pwd → Prints the present working directory
- cd <dir> → Change directory
- mkdir <dir> → Create directory
- rm -rf <dir/file> → Delete file or folder permanently
- cp <src> <dest> → Copy files
- mv <src> <dest> → Move/rename files
- cat <file> → Concatenate or read file content and prints on the stdout
- find → Seacrh for a file in a directory hierarchy
- wc <file> → Count lines, words and bytes

# 🌐 Networking troubleshooting
- ping → Check connectivity
- ip addr → Show IP address
- dig <domain> → DNS lookup
- nslookup <domain> → Resolve domain to IP
- curl → Transfer a URL or tool  for  transferring  data from or to a server using URLs [ Client URL ]
- netstat -tulnp → Show open ports & services

# 📊 System and Logs
- df -h → Disk usage
- systemctl start|status|stop <service> → Start a service | Check service status | Stop a service
- journalctl -u <service> → View service logs
- whoami → Current user
- history → Command history