# ⚙️ Process checks
1. ps -ef
    * Lists all running process
    * Shows PID, user, CPU usage etc
+ ```ps -ef | grep ssh```
    + Shows SSH-related running processes
![alt text](image.png)

2. top
    * Real-time dynamic monitoring
![alt text](image-1.png)

3. htop
    * Same as top but it provides additional interactive process viewer
![alt text](image-2.png)

# 🔧 Service checks
1. ```systemctl status ssh```
![alt text](image-3.png)
Service was active and running

2. ```systemctl list-units --type=service```
![alt text](image-4.png)
Display all active services

# 📄 Log Checks
1. ```journalctl -u nginx```
![alt text](image-5.png)
View nginx logs

2. ```tail -n 50 /var/log/syslog```
![alt text](image-6.png)
Shows last 50 lines of the log file
------------------------------------------------
# 🛠️ Mini troubleshooting steps
* We have checked if nginx service is running or not using ```systemctl status nginx```
* Logs verified using ```journalctl -u nginx```
* If service is down → restart using: ```sudo systemctl restart ssh```
* Again re-checked using ```systemctl status nginx```