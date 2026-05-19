Linux Architecture Basics
1. Kernel (Core of Linux)
Kernel Linux ka main part hota hai.
Ye hardware aur software ke beech bridge ka kaam karta hai.
Responsible for:
CPU management
Memory management
Device control
Process handling
File systems

Example:

Jab app RAM use karti hai → kernel manage karta hai.
Jab keyboard press hota hai → kernel hardware se communicate karta hai.
2. User Space
Jitne bhi normal programs hote hain wo user space me run karte hain.
Example:
Chrome
VS Code
Bash shell
Nginx

User directly kernel ko access nahi karta.
Programs → system calls → kernel.

3. Init / systemd
Linux boot hone ke baad sabse pehla process:
PID 1 = init/systemd
Modern Linux me mostly systemd use hota hai.
systemd ka kaam
Services start karna
Failed service restart karna
Boot process manage karna
Logs maintain karna (journald)

Example:

nginx automatically boot pe start karwana.

Command:

systemctl status nginx
Process Management
Process Kaise Create Hota Hai
Parent process fork() karta hai
Child process create hota hai
exec() new program load karta hai

Example:

Bash shell → command run → new process create.
Process States
State	Meaning
Running (R)	CPU use kar raha hai
Sleeping (S)	Wait kar raha hai
Stopped (T)	Manually stop hua
Zombie (Z)	Process finish ho gaya but entry bachi hai
Idle	Kuch kaam nahi
Zombie Process
Child process exit ho gaya
Parent ne status read nahi kiya
Too many zombies = issue

Check:

ps aux | grep Z
Important systemd Commands
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl status nginx
journalctl -u nginx
5 Daily Linux Commands
ps aux        # running processes
top           # live CPU/RAM usage
df -h         # disk usage
free -m       # memory usage
systemctl     # service management
Why This Matters in DevOps

Agar Linux processes aur systemd samajh aa gaya to:

Service crash jaldi debug kar sakte ho
CPU/RAM issue detect kar sakte ho
Logs efficiently check kar sakte ho
Production incidents fast solve kar sakte ho

Linux = DevOps ki foundation 🚀
