# Linux User Information Commands

---

## 1. Current User

1. **`whoami` / `logname`** → Show current username  

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ whoami
ubuntu
ubuntu@ip-172-31-6-93:~$ logname
ubuntu
````

---

## 2. Logged-in Users

1. **`users`** → List all logged-in users (names only)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ users
ubuntu ubuntu ubuntu
```

2. **`who`** → Show usernames + login time + terminal info

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ who
ubuntu   pts/0        2025-08-27 12:09 (163.223.49.125)
ubuntu   pts/1        2025-08-27 12:15 (163.223.49.125)
ubuntu   pts/2        2025-08-27 12:26 (163.223.49.125)
```

3. **`who -H`** → Same as `who` but with headers

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ who -H
NAME     LINE         TIME             COMMENT
ubuntu   pts/0        2025-08-27 12:09 (163.223.49.125)
ubuntu   pts/1        2025-08-27 12:15 (163.223.49.125)
ubuntu   pts/2        2025-08-27 12:26 (163.223.49.125)
```

---

## 3. User Activity

1. **`w`** → Display usernames + login time + idle time + what they are doing + system load

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ w
 13:22:54 up 21:27,  3 users,  load average: 0.00, 0.00, 0.00
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU  WHAT
ubuntu            163.223.49.125   12:26   20:33m  0.00s  0.01s sshd: ubuntu [priv]
ubuntu            163.223.49.125   12:15   20:33m  0.00s  0.01s sshd: ubuntu [priv]
ubuntu            163.223.49.125   12:09   20:33m  0.00s  0.01s sshd: ubuntu [priv]
```

2. **`last`** → Show login history

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ last
ubuntu   pts/3        163.223.49.125   Wed Aug 27 13:28   still logged in
ubuntu   pts/2        163.223.49.125   Wed Aug 27 12:26   still logged in
ubuntu   pts/1        163.223.49.125   Wed Aug 27 12:15   still logged in
ubuntu   pts/0        163.223.49.125   Wed Aug 27 12:09   still logged in
reboot   system boot  6.14.0-1011-aws  Tue Aug 26 15:55   still running
```

3. **`last -R username`** → Show login history for a specific user

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ last -R ubuntu
ubuntu   pts/3        Wed Aug 27 13:28   still logged in
ubuntu   pts/2        Wed Aug 27 12:26   still logged in
ubuntu   pts/1        Wed Aug 27 12:15   still logged in
ubuntu   pts/0        Wed Aug 27 12:09   still logged in
```

4. **`last -F`** → Show login/logout timestamps

---

## 4. Command Locations

1. **`whereis mkdir`** → Find binary, source, and man page locations

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ whereis mkdir
mkdir: /usr/bin/mkdir /usr/share/man/man1/mkdir.1.gz
```

