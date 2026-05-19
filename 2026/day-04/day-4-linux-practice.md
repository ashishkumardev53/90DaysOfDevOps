Linux Practice – Processes and Services

1. Process Checks
Check Running Processes
ps aux | head

Output:

USER       PID %CPU %MEM COMMAND
root         1  0.0  0.1 /sbin/init
root       645  0.0  0.2 systemd-journald
root       702  0.0  0.1 sshd
ashish    2103  0.1  0.5 bash

Observation:

PID 1 = init/systemd process
sshd service running tha
Real-Time Process Monitoring
top

Observation:

CPU usage low tha
Bash aur system processes visible the
Memory usage bhi check hui

2. Service Checks
Check SSH Service Status
systemctl status ssh

Output:

Active: active (running)
Loaded: loaded (/lib/systemd/system/ssh.service)

Observation:

SSH service properly running thi
List Running Services
systemctl list-units --type=service --state=running

Observation:

Multiple services running thi:
ssh
cron
systemd-journald

3. Log Checks
View SSH Logs
journalctl -u ssh --no-pager | tail -n 10

Output:

Started OpenBSD Secure Shell server
Accepted password for user
Session opened for user

Observation:

SSH login activity logs visible the
Check Last 20 System Logs
tail -n 20 /var/log/syslog

Observation:

Background services ke logs visible the
No major errors found

4. Mini Troubleshooting Flow
Problem:

SSH service running hai ya nahi verify karna tha.

Steps Performed
Step 1 – Check Service Status
systemctl status ssh

Result:

Service active mili
Step 2 – Check Process
pgrep sshd

Result:

sshd process PID show hua
Step 3 – Inspect Logs
journalctl -u ssh | tail

Result:

No failure logs found
Service healthy thi
What I Learned
Processes ko inspect karna
systemd services check karna
Logs read karna
Basic troubleshooting workflow samajhna

Ye commands production troubleshooting me bahut useful honge 🚀
