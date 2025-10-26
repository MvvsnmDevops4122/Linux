#  What is Linux?

Linux is an **open-source operating system (OS)**, similar in purpose to Windows or macOS.

Linux is secure and fast.

Is **case-sensitive** — for example, `kkfunda.txt` and `KKFUNDA.txt` are treated as two different files.  

It Was created in **1991 by Linus Torvalds**.

**Multitasking**: Can run multiple programs at the same time without slowing down or crashing.  

**Multi-user**: Supports multiple users accessing the system simultaneously without interfering with each other.

---

##  Free vs Open Source

### Free:
- Free means you can use the software without cost, but the source code is not available.  
- You **cannot see, modify, or improve** the code.  
- You cannot add your own features to it.

### Open Source:
- Open-source means the source code is freely available to everyone.  
- Anyone can **see, modify, improve, or share** the code.  
- You can add your own features to Linux and use it in your projects.

---

##  Basic Linux Architecture

- **Hardware** – Physical parts like CPU, RAM, disk, and input/output devices.  
- **Kernel** – The core of the OS; controls hardware like CPU, memory, and devices.  
- **Shell** – Interface to run commands and talk to the kernel (like bash).  
- **Utilities** – Command-line tools to manage files, monitor the system, control users, and handle networking.  
- **File System** – Organizes data into files and directories (everything is treated as a file).  
- **Applications** – Software like browsers, text editors, and tools that run on top of Linux.

<img width="686" height="371" alt="image" src="https://github.com/user-attachments/assets/b8cdc67c-d570-4e98-9fb7-44be6c5fa604" />

---

## 🐧 Some Popular Linux Distributions (Distros)

- **Ubuntu** – Best for beginners  
- **CentOS / AlmaLinux / Rocky** – Popular in servers  
- **Debian** – Stable and used in base distros  
- **Red Hat Enterprise Linux (RHEL)** – Enterprise and Commercial Use

🖼️ [Linux (Tux logo)] [Redhat] [CentOS] [openSUSE] [Ubuntu] [Fedora]

---

## 🔌 Some Tools to Connect to Linux Machines

- **Git Bash** – Popular on Windows for running Linux-like commands including SSH.  
- **PuTTY** – A lightweight SSH client for Windows, widely used for remote access.  
- **MobaXterm** – An advanced terminal for Windows with SSH, X11 forwarding, and many networking tools.  
- **macOS Terminal** – Built-in terminal on Macs, supports SSH natively.

<img width="628" height="202" alt="image" src="https://github.com/user-attachments/assets/7297f021-efdd-4c95-b0ca-64c93eb687c6" />

---

# 📁 Linux Directory Structure

---

<img width="824" height="512" alt="image" src="https://github.com/user-attachments/assets/eedd343d-5359-4a9e-9926-921685ffce49" />

----

## 1. `/` — Root Directory : 

This is the top-level directory in Linux. Everything starts from /

👉 Lists all top-level directories like `/bin`, `/etc`, `/home`, `/tmp`, etc.

---

## 2. `/root` → Root User’s Home Directory

This is the personal directory of the root (admin) user.

👉 Goes to the root user’s home and lists hidden files like `.bashrc`, `.ssh`, etc.

---

## 3. `/bin` → Basic Commands for All Users

This folder contains the essential command information stored in the /bin directory.

It contains the core executable files (binaries) for basic Linux commands like:

Contains essential user commands like ls, cp, cat, mv, rm.

👉 Lists first 10 commands available in `/bin`.

---

## 4. /boot – Booting Files

Contains the bootloader and kernel files required to start the Linux system.

## 5. `/etc` → System Configuration Files

Contains all configuration files for services and applications.

---

## 6. `/sbin` → System Administration Commands

Like /bin, but contains system-level commands reserved for the root user or users with sudo privileges.

👉 Lists system admin binaries like `shutdown`, `reboot`, `ifconfig`.

---

## 7. /lib – Shared Libraries

Contains shared library files that help programs in /bin and /sbin run.

Comparable to .dll files in Windows.

Essential for:

System commands

Boot processes

Core programs

---

## 8. `/opt` → Optional (Third-Party) Software

Used for installing third-party or extra software.

---
## 9. `/home` → User Home Directories

Each user gets a directory here (e.g., /home/satya, /home/dev).

👉 Lists all users’ home directories.

---

## 10. `/tmp` → Temporary Files

The /tmp directory is used to store temporary files created by the system or users.

👉 Creates a temporary file in `/tmp`.

```
