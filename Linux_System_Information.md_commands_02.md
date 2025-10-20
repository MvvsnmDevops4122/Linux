## 1. System Information Commands

---

### User Switching & Session

```bash
1. sudo su -                # Switch to root user (root's home: /root)
2. sudo su                  # Switch to root but stay in current user’s home directory
3. su - username            # Switch to another normal user
4. exit                     # Exit current shell/session
5. clear                    # Clear terminal screen
````

✅ **Use Case**: Switching between application users (e.g., `tomcat`, `jenkins`, `root`) during deployments or troubleshooting.

---

### Kernel & OS Info

```bash
1. uname                   # Show OS details (e.g., Linux)
2. uname -r                # Show kernel version
3. uname -a                # Full system info (kernel, OS, arch, build time)
4. uname -m                # Architecture (32/64-bit)
```

✅ **Use Case**: Checking kernel version before installing Docker/Kubernetes.

---

### Hostname & Network

```bash
1. hostname                            # Show hostname
2. hostname -i                         # Show system IP
3. hostnamectl set-hostname <name>    # Change hostname
```

✅ **Use Case**: Updating hostname to meaningful names like `jenkins-server`, `prod-db`.

---

### Uptime & Boot Time

```bash
1. uptime                  # Display system running time, users, load average
2. uptime -p               # Display running time only (e.g., up 2 hours)
3. uptime -s               # Show exact boot time
```

✅ **Use Case**: Checking server uptime after patching or unexpected reboot.

---

### History

```bash
1. history                 # Show executed commands
2. history -c              # Clear all history
3. history -d 500          # Delete entry #500
4. !35                     # Run command #35 from history
5. !!                      # Re-run the last executed command
```

✅ **Use Case**: Re-running long commands quickly during builds or troubleshooting.
⚠️ **Caution**: Avoid `history -c` on shared servers (audit trail loss).

---

### Manual & Help

The man command is used to view the manual pages for Linux commands and programs.

```bash
1. man <cmd>               # Manual page for command
2. whatis ls               # One-line description of the command
```

✅ **Use Case**: Quick help for unfamiliar commands.

---

### Date & Time

```bash
1. date                                      # Show system date/time
2. sudo date -s "2025-08-30 09:00:00"        # Set date/time
3. timedatectl                               # Show timezone & clock info
4. timedatectl set-timezone Asia/Kolkata     # Set timezone
```

✅ **Use Case**: Fixing incorrect timezone on Jenkins build servers.

---

### Date Format Examples

```bash
1. date +"%d"            # Display date only
2. date +"%m"            # Display month only
3. date +"%y"            # Display year only
4. date +%D              # MM/DD/YY
5. date +"%F"            # YYYY-MM-DD
6. date +"%A"            # Weekday name
7. date +"%B"            # Month name
8. date +%H:%M:%S        # Display Hours:Minutes:Seconds
```

✅ **Use Case**: Creating daily log files, e.g., `backup_$(date +"%F").log`

---

### Calendar

```bash
cal                    # Display current month calendar
```

✅ **Use Case**: Checking calendar while scheduling cron jobs.

---
