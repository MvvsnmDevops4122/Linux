# 🗂 Linux Directory Structure

---

## 1. `/` → Root directory
* This is the top-level directory in Linux. Everything starts from `/`.

**Example 1: List top-level directories**

```bash
ubuntu@ip-172-31-6-93:~$ ls /
bin                dev   lib                lost+found  opt   run                 snap  tmp
bin.usr-is-merged  etc   lib.usr-is-merged  media       proc  sbin                srv   usr
boot               home  lib64              mnt         root  sbin.usr-is-merged  sys   var
````

👉 Lists all top-level directories like `/bin`, `/etc`, `/home`, `/tmp`, etc.

**Example 2: Change to root directory**

```bash
ubuntu@ip-172-31-6-93:~$ cd /
ubuntu@ip-172-31-6-93:/$ pwd
/
```

👉 Changes current location to the root directory and prints `/`.

---

## 2. `/root` → Root user’s home directory

* This is the personal directory of the root (admin) user.

**Example: List hidden files in root’s home**

```bash
root@ip-172-31-6-93:~# cd /root && ls -a
.  ..  .bash_history  .bashrc  .profile  .ssh  snap
```

👉 Goes to the root user’s home and lists hidden files like `.bashrc` and `.ssh`.

---

## 3. `/bin` → Basic user commands

* Contains essential user commands like `ls`, `cp`, `cat`, `mv`, `rm`.

**Example: List first 10 commands**

```bash
root@ip-172-31-6-93:~# ls /bin | head
NF
VGAuthService
[
aa-enabled
aa-exec
aa-features-abi
acpi_listen
acpidbg
add-apt-repository
addpart
```

👉 Lists first 10 commands available in `/bin`.

---

## 4. `/sbin` → System administration commands

* Contains system-level commands (normally used by root).

**Example: List first few binaries**

```bash
root@ip-172-31-6-93:~# ls /sbin | head
ModemManager
aa-load
aa-remove-unknown
aa-status
aa-teardown
accessdb
acpid
add-shell
addgnupghome
addgroup
```

👉 Lists system admin binaries like `shutdown`, `reboot`, `ifconfig`.

---

## 5. `/opt` → Optional (third-party) software

* Used for installing third-party or extra software.

**Example: List installed third-party applications**

```bash
root@ip-172-31-6-93:~# ls /opt
```

👉 Example: `/opt/google`, `/opt/tomcat`.

---

## 6. `/etc` → System configuration files

* Contains all configuration files for services and applications.

**Example 1: Find SSH configuration files**

```bash
root@ip-172-31-6-93:/opt# ls /etc | grep ssh
ssh
```

**Example 2: Display system hostname**

```bash
root@ip-172-31-6-93:~# cat /etc/hostname
ip-172-31-6-93
```

---

## 7. `/home` → User home directories

* Each user gets a directory here (e.g., `/home/satya`, `/home/dev`).

**Example: List all users’ home directories**

```bash
root@ip-172-31-6-93:~# ls /home
ubuntu
```

---

## 8. `/tmp` → Temporary files

* Used for temporary storage. Cleared after reboot.

**Example: Create a temporary file**

```bash
root@ip-172-31-6-93:~# touch /tmp/testfile
root@ip-172-31-6-93:~# ls -l /tmp/testfile
-rw-r--r-- 1 root root 0 Aug 27 17:46 /tmp/testfile
```

👉 Creates a temporary file in `/tmp`.

```
