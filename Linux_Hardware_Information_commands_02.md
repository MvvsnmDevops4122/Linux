# Linux Hardware Information Commands
---

## 1. CPU Information

```bash

1. lscpu                  # Show CPU architecture details (cores, threads, vendor)

2. cat /proc/cpuinfo      # CPU hardware info

3. nproc                  # Number of CPU cores available

---

## 2. Memory Information

```bash

4. free                   # Show memory usage

5. free -h                # Show Memory in human-readable format

6. free -m                # Show Memory in MB

---

## 3. System Statistics

```bash

6. vmstat                 # Shows CPU, memory, swap, and I/O  statistics

```

ubuntu@ip-172-31-6-93:~$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- -------cpu-------
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st gu
 2  0      0 185280  22120 536036    0    0     9    15   43    0  0  0 100  0  0  0

---

## 4. top

```bash

7. top                    # Display Real-time process & resource monitor

```
