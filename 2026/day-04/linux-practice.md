# Day 4 – Linux Practice: Processes and Services

> Services like ssh, nginx, docker, cron, ping

## ⚙️ Process checks
1. ```ps -ef``` → Provides snapshot of all running processes.

![alt text](image.png)

* ```ps -ef | grep ssh``` → Shows SSH-related running processes.

![alt text](image-1.png)


2. ```top``` → Provides dynamic real-time view of all the running processes.

![alt text](image-2.png)

* ```htop``` → Same as top with additional features like  interactive process viewer; we can scroll horizontally & vertically.

![alt text](image-3.png)


3. ```pgrep <service>``` → Find PID of a process.

![alt text](image-4.png)

---

## 🔧 Service checks
1. ```systemctl status ssh``` → Check service status/health; service is active and running.

![alt text](image-5.png)


2. ```systemctl list-units --type=service``` → Display all active/running services

![alt text](image-6.png)

> “Linux services are managed by systemd using systemctl commands.”

---

## 📄 Log checks
1. ```journalctl -u nginx``` → View nginx logs.

![alt text](image-7.png)

* ```journalctl -xe``` → Recent errors.

![alt text](image-8.png)


2. ```tail -n 20 /var/log/syslog``` → Shows last 20 lines of system log file.

![alt text](image-9.png)

---

## 🛠️ Mini troubleshooting steps
1. Check service statsus 
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