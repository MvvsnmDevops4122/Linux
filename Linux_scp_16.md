# 🔐 SCP Command (Secure Copy)

`scp` stands for **Secure Copy Protocol**.  
It is used to **securely transfer files or directories** between:

- Local system → Remote system  
- Remote system → Local system  
- Remote system → Remote system  

It uses **SSH encryption**, so it is secure.

# 📦 SCP Commands (PowerShell & Git Bash)

Below are the correct SCP commands for both **Windows PowerShell** and **Git Bash**.

---

## 🟦 PowerShell
Use **Windows-style paths** with **double quotes**.

### ✅ Upload file (Local → EC2)
```

scp -i "C:\Users\satya\Downloads\KKDevops1.pem" "C:\Users\satya\Downloads\Jenkins_Notes_KKdevops" ec2-user@52.66.252.67:/home/ec2-user/

```

### ✅ Download file (EC2 → Local)
```

scp -i "C:\Users\satya\Downloads\KKDevops1.pem" ec2-user@52.66.252.67:/home/ec2-user/hello.sh "C:\Users\satya\Downloads"

```

---

## 🟩 Git Bash
Use **Linux-style paths** starting with `/c/...`

### ✅ Upload file (Local → EC2)
```

scp -i /c/Users/satya/Downloads/KKDevops1.pem /c/Users/satya/Downloads/Jenkins_Notes_KKdevops ec2-user@52.66.252.67:/home/ec2-user/

```

### Explanation

-i /c/Users/satya/Downloads/KKDevops1.pem → Your key

/c/Users/satya/Downloads/Jenkins_Notes_KKdevops → Source

ec2-user@52.66.252.67 → EC2 username + public IP

/home/ec2-user/ → Upload destination

### ✅ Download file (EC2 → Local)
```

scp -i /c/Users/satya/Downloads/KKDevops1.pem ec2-user@52.66.252.67:/home/ec2-user/hello.sh /c/Users/satya/Downloads/

```

---

# 📝 Notes
- PowerShell → Use `"C:\path\to\file"`  
- Git Bash → Use `/c/path/to/file`  
- Both require **inbound SSH (port 22)** allowed in AWS Security Group  
- `.pem` file should have correct permissions:  
```

chmod 400 <key>.pem    # (only required in Git Bash)

```

---

