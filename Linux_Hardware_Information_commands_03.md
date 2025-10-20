# (2) Hardware Information Commands

##  Basic CPU & Memory Commands

```bash
1. lscpu                  # Show CPU architecture details (cores, threads, vendor)
2. cat /proc/cpuinfo      # CPU hardware info
3. nproc                  # Number of CPU cores available
4. free                   # Show memory usage
5. free -h                # Show memory in human-readable format
6. free -m                # Show memory in MB
7. vmstat                 # Show CPU, memory, swap, and I/O statistics
8. top                    # Display real-time process & resource monitor
````

---

## 📊 `vmstat` Example Output:

```bash
ubuntu@ip-172-31-6-93:~$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- -------cpu-------
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st gu
 2  0      0 185280  22120 536036    0    0     9    15   43    0  0  0 100  0  0  0
```

---

✅ **Use Case**:
Check **CPU, RAM**, and **system load** before deploying heavy applications like **Jenkins**, **MySQL**, or other services.
---
