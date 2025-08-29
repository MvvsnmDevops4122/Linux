# Linux Hardware Information Commands
---

## 1. CPU Information

1.  **`lscpu`** → Show CPU architecture details (cores, threads, vendor)

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ lscpu
Architecture:                x86_64
CPU op-mode(s):              32-bit, 64-bit
Address sizes:               46 bits physical, 48 bits virtual
Byte Order:                  Little Endian
CPU(s):                      2
On-line CPU(s) list:         0,1
Vendor ID:                   GenuineIntel
Model name:                  Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
CPU family:                  6
Model:                       85
````

2. **`cat /proc/cpuinfo`** → CPU hardware info

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ cat /proc/cpuinfo
processor       : 0
vendor_id       : GenuineIntel
cpu family      : 6
model           : 85
model name      : Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
stepping        : 7
microcode       : 0x5003901
cpu MHz         : 2499.998
cache size      : 36608 KB
physical id     : 0
```

3. **`nproc`** → Number of CPU cores available

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ nproc
2
```

---

## 2. Memory Information

1. **`free`** → Show memory usage

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ free
               total        used        free      shared  buff/cache   available
Mem:          936164      363780      185280        2796      558112      572384
Swap:              0           0           0
```

2. **`free -h`** → Show memory in human-readable format

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ free -h
               total        used        free      shared  buff/cache   available
Mem:           914Mi       355Mi       180Mi       2.7Mi       545Mi       558Mi
Swap:             0B          0B          0B
```

3. **`free -m`** → Show memory in MB

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ free -m
               total        used        free      shared  buff/cache   available
Mem:             914         355         180           2         545         558
Swap:              0           0           0
```

4. **`free -g`** → Show memory in GB

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ free -g
               total        used        free      shared  buff/cache   available
Mem:               0           0           0           0           0           0
Swap:              0           0           0
```

---

## 3. System Statistics

1. **`vmstat`** → Show CPU, memory, swap, and I/O statistics

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- -------cpu-------
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st gu
 2  0      0 185280  22120 536036    0    0     9    15   43    0  0  0 100  0  0  0
```

2. **`top`** → Display real-time process & resource monitor

✅ Example:

```bash
ubuntu@ip-172-31-6-93:~$ top
top - 13:07:22 up 21:12,  3 users,  load average: 0.00, 0.00, 0.00
Tasks: 113 total,   1 running, 112 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.2 sy,  0.0 ni, 99.8 id,  0.0 wa,  0.0 hi,  0.0 si, 0.0 st
MiB Mem :    914.2 total,    180.9 free,    355.2 used,    545.1 buff/cache
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    559.1 avail Mem
```
