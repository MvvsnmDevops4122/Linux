# 📅 Crontab: Scheduling Tasks

## 🔧 Syntax :

```

* * * * * /path/to/command

---

| | | | |
| | | | +---- Day of the Week (0 - 6) (Sunday = 0 or 7)
| | | +------ Month (1 - 12)
| | +-------- Day of the Month (1 - 31)
| +---------- Hour (0 - 23)
+------------ Minute (0 - 59)

```

## Cron Commands

| Command              | Description                                       |
|----------------------|---------------------------------------------------|
| `crontab -l`         | List all scheduled cron jobs for current user     |
| `crontab -e`         | Edit crontab                                      |
| `crontab -r`         | Remove crontab                                    |
| `crontab -l -u <user>` | View another user's crontab (root only)        |

---

## 🔐 Control Cron Access:

```

sudo touch /etc/cron.allow       # Create allow file
sudo vi /etc/cron.allow          # Add allowed usernames (one per line)

````

---

## 📝 Sample Shell Script – hello.sh

```bash
#!/bin/bash
echo "Welcome to KK FUNDA"
echo "Today date is:"
date
uptime
pwd
````

---

## ▶️ Run the Script

```
sh hello.sh          # Method 1
./hello.sh           # Method 2 (needs execute permission)
chmod u+x hello.sh   # Add execute permission
```

---

## ⏰ Schedule Script in Cron

Add to `crontab -e`:

```
*/1 * * * * /home/ec2-user/hello.sh >> /home/ec2-user/hello.log
```

📝 Use `>>` to append output and preserve logs.
