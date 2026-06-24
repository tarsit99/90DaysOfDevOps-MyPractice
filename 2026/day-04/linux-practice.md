# Day 4 – Linux Practice: Processes and Services

> Services like nginx, docker, ssh, ping, cron

## ⚙️ Process checks
1. ```ps -ef``` → Provides snapshot of all running processes.

![ps -ef command snap](image.png)

* ```ps -ef | grep ssh``` → Shows SSH-related running processes.

![ps -ef | grep ssh command snap](image-1.png)


2. ```top``` → Provides dynamic real-time view of all the running processes.

![top command snap](image-2.png)

* ```htop``` → Same as top with additional features like  interactive process viewer; we can scroll horizontally & vertically.

![htop command snap](image-3.png)


3. ```pgrep <service>``` → Find PID of a process.

![pgrep command snap](image-4.png)

---

## 🔧 Service checks
1. ```systemctl status ssh``` → Check service status or health; service is active and running.

![systemctl status command snap](image-5.png)


2. ```systemctl list-units --type=service``` → Display all active/running services

![systemctl list units command snap](image-6.png)

> “Linux services are managed by systemd using systemctl commands.”

---

## 📄 Log checks
1. ```journalctl -u nginx``` → View nginx logs.

![journalctl log check command snap](image-7.png)

* ```journalctl -xe``` → Recent errors.

![recent error using journalctl command snap](image-8.png)


2. ```tail -n 20 /var/log/syslog``` → Shows last 20 lines of system log file.

![tail command snap](image-9.png)

---

## 🛠️ Mini troubleshooting steps
1. Check service status 
```systemctl status <service>```

2. Check logs
```journalctl -u <service>```

3. Restart service if required or service is down
```sudo systemctl restart <service>```

4. Verify process
```systemctl status <service>``` or ```pgrep <serviceName>```

### 🧠 Memory Tip
Status → Logs → Restart → Verify

---

## 📌 Commands to Rmember (Must-Know)
```ps -ef```
```htop```
```pgrep```
```systemctl status```
```systemctl list-units --type=service```
```journalctl -u```
```tail -n```