Linux Commands Cheat Sheet 🚀

Process Management
   
View Running Processes

ps aux

Sabhi running processes dikhata hai.

Real-Time System Monitoring

top

Live CPU aur RAM usage monitor karta hai.

Better System Monitor

htop

Interactive process viewer.

Kill a Process

kill PID

Specific process stop karta hai.

Force Kill Process

kill -9 PID

Forcefully process terminate karta hai.

Background Jobs

jobs

Current shell ke background jobs dikhata hai.

Run Process in Background

command &

Command ko background me run karta hai.

Process Tree

pstree

Parent-child process structure dikhata hai.

File System Commands
   
Current Directory

pwd
Current working directory dikhata hai.

List Files

ls -la

Hidden files ke sath detailed list.

Change Directory

cd folder_name

Folder change karta hai.

Create File

touch file.txt

Empty file create karta hai.

Create Directory

mkdir test

New folder banata hai.

Copy Files

cp file1 file2

File copy karta hai.

Move/Rename File

mv old.txt new.txt

File move ya rename karta hai.

Delete File

rm file.txt

File remove karta hai.

Delete Directory

rm -r folder

Folder recursively delete karta hai.

View File Content

cat file.txt

File content show karta hai.

Read Large Files

less logfile.log

Large files easily read karne ke liye.

Search Text

grep "error" logfile.log

File me text search karta hai.

Disk Usage

df -h

Disk space usage dikhata hai.

Folder Size

du -sh folder

Folder ka total size dikhata hai.

5. Networking Troubleshooting
6. 
Check Connectivity

ping google.com

Network reachable hai ya nahi check karta hai.

Show IP Address

ip addr

System IP address details dikhata hai.

DNS Lookup

dig google.com

DNS resolution check karta hai.

Test HTTP Request

curl https://example.com

Website/API response test karta hai.

Open Ports

ss -tulnp

Listening ports aur services dikhata hai.

Network Path Trace

traceroute google.com

Packet kis route se ja raha hai dikhata hai.

 Log & Service Commands
 
View System Logs

journalctl

System logs show karta hai.

Service Status

systemctl status nginx

Service running hai ya nahi check karta hai.

Restart Service

systemctl restart nginx

Service restart karta hai.

Follow Logs Live

tail -f app.log

Live log monitoring.

Why These Commands Matter for DevOps

Ye commands help karte hain:

Crashed service debug karne me

CPU/RAM issue identify karne me

Network problems troubleshoot karne me

Logs inspect karne me

Production downtime reduce karne me

Linux command line mastery = Strong DevOps foundation 🔥
