## 📂 File and Directory Management in Linux

---

## 1🔹 Listing & Checking Location of Files and Directories

| Command | Description |
|----------|-------------|
| `ls` | List files and directories |
| `ls -l` | Display detailed info (permissions, owner, size, etc.) |
| `ls -a` | Show hidden and normal files/folders (starting with `.`) |
| `ls -lh` | Human-readable sizes (KB, MB, etc.) |
| `ls -lr` | Show files in reverse order |
| `ls -lt` | Sort by modification time (newest to oldest) |
| `ls -i` | Show inode numbers |
| `ls -lrthai` | All-in-one view (detailed, reverse, time, human-readable, inode) |
| `pwd` | Show current working directory |

---

## 2🔹 Change Directories Commands

| Command | Description |
|----------|-------------|
| `cd /path` | Go to a specific directory |
| `cd` | Go to home directory |
| `cd -` | Go to previous directory |
| `cd ../` | Move one directory back |
| `cd ../../` | Move two directories back |

---

## 3🔹 Display Directory Structure

| Command | Description |
|----------|-------------|
| `tree` | Show directory structure in tree format |

---

## 4🔹 Creating Files & Directories Commands

| Command | Description |
|----------|-------------|
| `touch filename` | Create an empty file |
| `touch one two three` | Create multiple empty files |
| `mkdir -v foldername` | Create a directory (verbose output) |
| `mkdir folder1` | Create a single directory |
| `mkdir fold1 fold2 fold3` | Create multiple directories |
| `mkdir -p parent/child1/child2/child3` | Create nested directories |

---

## 5🔹 Removing Files & Directories Commands

| Command | Description |
|----------|-------------|
| `rm filename` | Remove an empty file |
| `rm *` | Remove all files in the current directory |
| `rm -rf` | Force remove non-empty files/directories |
| `rmdir foldername` | Remove an empty directory |
| `rmdir *` | Remove all empty directories |
| `rm -rf foldername` | Remove non-empty directories/files |

---

## 📋 Copy / Move / Rename Files and Directories

### 6🔹 Copy Files or Directories (`cp`)

| Command | Description |
|----------|-------------|
| `cp devops.txt DevOps/` | Copy file → directory |
| `cp -r Python DevOps/` | Copy directory → directory (recursively) |
| `cp file1.txt file2.txt` | Copy file → file |
| `cp *.java destination_dir/` | Copy all `.java` files to a directory |

---

### 7🔹 Move or Rename (`mv`)

| Command | Description |
|----------|-------------|
| `mv python.txt devops.txt` | Rename file |
| `mv DevOps/ Python/` | Move directory |

---

## 8.🔍 File Comparison

### 🔹 View Files Page-by-Page (`more`)

```bash
more file1 file2
````

**Example Output:**

```
::::::::::::::
file1
::::::::::::::
Hello file one
Thanks for joining
::::::::::::::
file2
::::::::::::::
Hello file two
Thanks for joining
```

---

### 🔹 Compare Files Line-by-Line (`diff`)

| Command               | Description                    |
| --------------------- | ------------------------------ |
| `diff file1 file2`    | Compare two files line-by-line |
| `diff -y file1 file2` | Show side-by-side comparison   |

**Example:**

```
diff file1 file2
< Hello file one
---
> Hello file two
```

---

## 9.🧾 View / Create / Append / Copy / Merge Files (cat Command)

| Command                       | Description                              |
| ----------------------------- | ---------------------------------------- |
| `cat file.txt`                | View contents of a file                  |
| `cat file1 file2`             | View multiple files                      |
| `cat > newfile.txt`           | Create a new file (press Ctrl+D to save) |
| `cat >> existingfile.txt`     | Append content to an existing file       |
| `cat file1 file2 > merge.txt` | Merge two files into a new file          |
| `cat -n file.txt`             | Show file content with line numbers      |
| `tac file.txt`                | Show file content in reverse order       |

---

## 10. Nullifying a file

```bash
> file.txt                         # clearing its content without deleting the file itself.
```
---

## 11. head (View First N Lines of a File)

Description: The head command displays the first few lines of a file.

Usage:
```bash
head file.txt  # Show first 10 lines
head -n 3 file.txt  # Show first 3 lines
head -3 file.txt  # Alternative syntax
```
Display Specific Line Range (35-50) from a 100-Line File:

```bash
head -50 file.txt | tail -15
```
---

 ## 7. tail (View Last N Lines of a File)
 
Description: The tail command displays the last few lines of a file.

Usage:

```bash
tail file.txt  # Show last 10 lines
tail -n 3 file.txt  # Show last 3 lines
tail -3 file.txt  # Alternative syntax
```
Multiple Files:

```bash
tail file1.txt file2.txt  # Show last 10 lines of both files
tail -q file1.txt file2.txt  # Suppress headers while displaying output
```
