# ⚙️ Process management
- ps -ef → List all running processes
- top → Dynamic real-time CPU/memory usage
- htop → Interactive process viewer, similar to top but allows you to scroll vertically and horizontally, and interact using a pointing device (mouse)
- kill <PID> → Terminate a process
- kill -9 <PID> → Force kill process
- free -m → Check memory usage
- nproc → prints the number of processing units (CPU cores) available to the current process
- uptime → System load & uptime

# 📁 File system commands
- ls -l → Long Listing files
- pwd → Show present working directory
- cd <dir> → Change directory
- mkdir <dir> → Create directory
- rm -rf <dir/file> → Delete file or folder permanently
- cp <src> <dest> → Copy files
- mv <src> <dest> → Move/rename files
- cat <file> → Concatenate or read file content
- find → Seacrh for a file in a directory hierarchy
- wc → Print newline, word and byte counts for each file

# 🌐 Networking troubleshooting
- ping → Check connectivity
- ip addr → View IP address
- dig <domain> → DNS lookup utility
- nslookup → Name to IP resolution
- curl → Transfer a URL or tool  for  transferring  data from or to a server using URLs
- netstat -tulnp → Check open ports

# 📊 System and Logs
- df -h → Disk usage
- systemctl start|status|stop <service> → Start a service | Check service health | Stop a service
- journalctl -u <service> → View service logs
- whoami → Current user
- history → Command history