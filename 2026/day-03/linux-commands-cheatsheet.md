# Day 03 – Linux Commands Cheatsheet

## ⚙️ Process management
- ```top``` → Display dynamic real-time CPU/memory usage & active processes.
- ```htop``` → Interactive process viewer, similar to top but allows you to scroll vertically and horizontally.
- ```ps aux``` → Provide a detailed snapshot of all running processes. It is a common technique used for system troubleshooting and monitoring.
- ```kill -9 <PID>``` → Forcefully terminate a process.
- ```free -m``` → Display memory usage.
- ```nproc``` → Show number of CPU cores.
- ```uptime``` → Tell how long the system has been running & load average.

## 📁 File system commands
- ```ls -l``` → List files in long format.
- ```pwd``` → Prints the current working directory.
- ```cd <dir>``` → Change directory.
- ```mkdir <dir>``` → Create a new directory.
- ```rm -rf <dir/file>``` → Forcefully & recursively removes files/folder.
- ```cp <src> <dest>``` → Copy files/directories.
- ```mv <src> <dest>``` → Move/rename files/directories.
- ```cat <file>``` → Concatenate files and prints on the standard output (stdout).
- ```find``` → Seacrh for a file in a directory hierarchy.
- ```wc <file>``` → Count the no. lines, words and bytes.
- ```df -h``` → Show disk space usage across all mounted file system.

## 🌐 Networking troubleshooting
- ```ping <host>``` → Check connectivity whether a host is reacheable or not.
- ```ip addr``` → Show IP address & other network interface details.
- ```dig <domain>``` or ```nslookup <domain>``` → DNS lookup to check domain-to-IP mapping.
> - dig -> domain information grofer
- ```curl -I <url>``` → Fetch the HTTP header for a website (great for debugging 404/500 error).
> - curl -> client uniform resource locater
- ```netstat -tulnp``` → Lists all listening ports and applications using them

## 📊 System and Logs
- ```systemctl start|status|stop <service>```→ Start a service | Check service status | Stop a service.
- ```journalctl -u <service>``` → Shows logs for a service.
- ```whoami``` → Current user.
- ```history``` → Check command history.
- ```which bash``` → Shows which shell.