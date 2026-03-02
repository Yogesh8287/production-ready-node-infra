# 1️⃣ Introduction to Linux

## What is Linux?

* Linux is a **Unix-like, open-source operating system kernel**
* Created by **Linus Torvalds** in 1991
* It powers:

  * Servers 🌐
  * Cloud platforms ☁️
  * Android 📱
  * Supercomputers 🖥️

---

## 🏗 Linux Architecture

![Image](https://www.scaler.com/topics/images/fundamental-architecture-of-linux.webp)

### Layers:

1. Hardware
2. Kernel
3. Shell
4. User Applications

---

## 🔥 Kernel Responsibilities - Written in C

* Process Management
* Memory Management
* File System Handling
* Device Drivers
* System Calls

---

# 2️⃣ Linux File System

## 📂 File System Hierarchy

![Image](https://miro.medium.com/0%2AbFnHaO8eYpW3dSuz)

| Directory | Purpose              |
| --------- | -------------------- |
| `/`       | Root directory       |
| `/home`   | User files           |
| `/etc`    | Configuration files  |
| `/bin`    | Basic binaries       |
| `/var`    | Logs & variable data |
| `/usr`    | User programs        |
| `/dev`    | Device files         |
| `/proc`   | Process information  |

---

## 📌 File Types

* `-` → Regular file
* `d` → Directory
* `l` → Symbolic link
* `c` → Character device
* `b` → Block device

---

# 3️⃣ Important Linux Commands

## 🔹 File & Directory Commands

```bash
pwd
ls
ls -la
cd
mkdir
rmdir
rm -rf
cp
mv
touch
```

---

## 🔹 Viewing Files

```bash
cat
less
more
head
tail
tail -f
```

---

## 🔹 Search & Filter

```bash
grep
find
locate
which
whereis
```

Example:

```bash
grep "error" file.txt
```

---

# 4️⃣ File Permissions & Ownership

## Permission Structure

Example:

```bash
-rwxr-xr--
```

Breakdown:

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

## Permission Levels

* User (Owner)
* Group
* Others

---

## Change Permission

```bash
chmod 755 file.sh
chmod +x script.sh
```

## Change Ownership

```bash
chown user file.txt
chown user:group file.txt
```

---

# 5️⃣ Process Management

## View Processes

```bash
ps aux
top
htop
```

## Kill Process

```bash
kill PID
kill -9 PID
```

## Background Process

```bash
command &
jobs
fg
bg
```

---

# 6️⃣ Package Management

### Debian-based (Ubuntu)

```bash
sudo apt update
sudo apt upgrade
sudo apt install nginx
```

### RHEL-based (CentOS)

```bash
sudo yum install httpd
```

---

# 7️⃣ Shell & Bash Scripting

## What is Shell?

Interface between user and kernel.

Popular shell:

* Bash
* Zsh
* Sh

---

## Basic Bash Script

```bash
#!/bin/bash
echo "Hello Yogesh"
```

Run:

```bash
chmod +x script.sh
./script.sh
```

---

## Variables

```bash
name="Yogesh"
echo $name
```

---

## If Condition

```bash
if [ $a -gt 10 ]
then
 echo "Greater"
fi
```

---

# 8️⃣ Networking in Linux

## Check IP

```bash
ip a
ifconfig
```

## Ping

```bash
ping google.com
```

## Check Open Ports

```bash
netstat -tulnp
ss -tulnp
```

---

# 9️⃣ Disk & Memory Management

## Disk Usage

```bash
df -h
du -sh *
```

## Mount

```bash
mount
umount
```

---

# 🔟 User Management

```bash
adduser yogesh
passwd yogesh
usermod
groupadd
```

---

# 1️⃣1️⃣ System Logs

Logs stored in:

```bash
/var/log/
```

Example:

```bash
/var/log/syslog
/var/log/auth.log
```

---

# 1️⃣2️⃣ Systemctl (Service Management)

```bash
systemctl start nginx
systemctl stop nginx
systemctl status nginx
systemctl enable nginx
```

---

# 1️⃣3️⃣ Cron Jobs

Edit cron:

```bash
crontab -e
```

Example:

```
* * * * * /path/script.sh
```

Format:

```
MIN HOUR DOM MON DOW
```

---

# 1️⃣4️⃣ Advanced Concepts (Interview Level)

* Soft Link vs Hard Link
* Inode
* Load Average
* Zombie Process
* Swap Memory
* SSH
* Environment Variables
* Pipes & Redirection

Example:

```bash
ls -l | grep ".txt"
```

Redirection:

```bash
>   (overwrite)
>>  (append)
2>  (error redirect)
```
