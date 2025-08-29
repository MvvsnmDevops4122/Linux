# Linux System Information Commands

---

## 1. User Switching & Session

1. **`sudo su -` (OR) `sudo -i`** → Switch to root user (root’s home: `/root`)  

✅ Example:
```bash
ubuntu@ip-172-31-6-93:~$ sudo su -
root@ip-172-31-6-93:~# pwd
/root
````

2. **`sudo su`** → Switch to root but stay in current user’s home directory

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ sudo su
root@ip-172-31-6-93:/home/ubuntu# pwd
/home/ubuntu
```

3. **`su - username`** → Switch to another normal user

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ su - john
john@ip-172-31-6-93:~$ whoami
john
```

4. **`exit`** → Exit current shell/session

✅ Example:

```bash
root@ip-172-31-6-93:~# exit
logout
ubuntu@ip-172-31-6-93:~$
```

5. **`clear`** → Clear terminal

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ clear
# (screen is cleared)
```

---

## 2. Kernel & OS

1. **`uname`** → Show OS details (e.g., Linux)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uname
Linux
```

2. **`uname -r`** → Show kernel version

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uname -r
6.14.0-1011-aws
```

3. **`uname -a`** → Full system info (kernel, OS, arch, build time)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uname -a
Linux ip-172-31-6-93 6.14.0-1011-aws #11~24.04.1-Ubuntu SMP Fri Aug  1 02:07:25 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux
```

4. **`uname -m`** → Show architecture (32/64-bit)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uname -m
x86_64
```

---

## 3. Hostname & Network

1. **`hostname` / `hostname -i`** → Show system hostname / Show system IP

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ hostname
ip-172-31-6-93
```

2. **`hostnamectl set-hostname <name>`** → Change hostname

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ sudo hostnamectl set-hostname satya
ubuntu@satya:~$
```

---

## 4. System Uptime

1. **`uptime`** → Display system running time along with number of users and load average

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uptime
11:11:07 up 45 min,  4 users,  load average: 0.00, 0.00, 0.00
```

2. **`uptime -p`** → Display system running time only

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uptime -p
up 47 minutes
```

3. **`uptime -s`** → Show exact system boot time

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ uptime -s
2025-08-26 15:55:10
```

---

## 5. History

1. **`history`** → Show executed commands

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ history
    1  sudo -i
    2  useradd satya
    3  useradd Ram
    4  useradd sai
    5  getent passwd
    6  clear
```

2. **`history -c`** → Clear all history

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ history
    1  history
```

3. **`history -d 500`** → Delete entry 500 from history

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ history -d 3
```

4. **`!2`** → Run command #2 from history

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ !2
pwd
/home/ubuntu
```

---

## 6. Manual & Help

1. **`man <cmd>`** → Show manual page

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ man pwd
```

2. **`man -f grep`** → One-line description (same as `whatis`)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ man -f grep
grep (1) - print lines that match patterns
```

3. **`whatis ls`** → Short description of ls

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ whatis ls
ls (1) - list directory contents
```

---

## 7. Date & Time

1. **`date`** → Show system date/time

✅ Example:

```bash
Wed Aug 27 12:15:36 IST 2025
```

2. **`timedatectl`** → Show time zone & clock info

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ timedatectl
               Local time: Wed 2025-08-27 12:19:28 IST
           Universal time: Wed 2025-08-27 06:49:28 UTC
                 RTC time: Wed 2025-08-27 06:49:27
                Time zone: Asia/Kolkata (IST, +0530)
System clock synchronized: yes
              NTP service: active
          RTC in local TZ: no
```

3. **`timedatectl set-timezone Asia/Kolkata`** → Set timezone

**Date Format Examples:**

```bash
date +%d       # Display date only
date +%m       # Display month only
date +%y       # Display year only
date +%H:%M:%S # Display Hours:Minutes:Seconds
date +%D       # MM/DD/YY
date +%F       # YYYY-MM-DD
date +%A       # Display day name
date +%B       # Display month name
```

---

## 8. Calendar

1. **`cal`** → Show current month’s calendar

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ cal
```

2. **`cal 2025`** → Show year calendar

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ cal 2025
```

```

