
# 🔗 **ln Command (Link Creation)**

The `ln` command in Linux is used to **create links between files**.  
There are two types of links:

1. **Hard Links**  
2. **Symbolic (Soft) Links**

<img width="745" height="366" alt="image" src="https://github.com/user-attachments/assets/3b86d6e9-47a9-4358-bfc8-6412c1f4655f" />

---

## 🧩 **Syntax**

```bash
ln originalfile linkfile         # Hard Link
ln -s originalfile linkfile      # Soft Link (Symbolic)
````

---

## 🧪 **Examples**

```bash
sudo ln devops.txt hardlink.txt      # Create a hard link
ln -s devops.txt softlink.txt        # Create a soft link (starts with 'l' in ls -l output)
```

---

## ⚖️ **Hard Link vs Soft Link**

| Feature                     | Hard Link                                                    | Soft Link (Symbolic)                                          |
| --------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------- |
| **1. Data Synchronization** | Data is synchronized                                         | Data is synchronized                                          |
| **2. Inode Number**         | Same inode number                                            | Different inode number                                        |
| **3. File Deletion**        | If original file is deleted, linked file is still accessible | If original file is deleted, linked file becomes inaccessible |
| **4. Usage**                | Only for files                                               | For files and folders                                         |

---

## 💡 **Use Cases**

* Create multiple names for one file without duplicating data.
* Maintain backup references.
* Organize directory access using symbolic links.
* Create shortcuts to config files or frequently accessed paths.

---
## 🪜 Step 1: How to Create Hardlink

```bash
ln originalfile.txt hardlink.txt
```

<img width="839" height="149" alt="image" src="https://github.com/user-attachments/assets/18a77ae8-1451-4c0c-915a-945acf8bf5c4" />

---
## 🔍 Step 2: Check the Inode Numbers

```bash
ls -li
```
<img width="880" height="135" alt="image" src="https://github.com/user-attachments/assets/46480694-88e7-4985-9f1c-5e8fb335666a" />

✅ Notice: Both have the same inode number.

---

## 📜 Step 3: Display the Content of Both Files

```bash
cat originalfile.txt
cat hardlink.txt
```
<img width="848" height="152" alt="image" src="https://github.com/user-attachments/assets/13efad6e-d30d-4ace-beeb-62c0917034df" />

Both show the same content, because they’re really the same file with two different names.

---

## ✏️ Step 4: Add New Content and Verify Data Sync

Let’s add a new line to the file using the echo command:
```bash
echo "This is project1" >> originalfile.txt
```
Next, check the contents of both files:

```bash
cat originalfile.txt
cat hardlink.txt
```
<img width="763" height="206" alt="image" src="https://github.com/user-attachments/assets/c5c618da-be1b-46a1-8dbd-dab1d4199eb5" />

✅ Notice: You’ll see the same data in both files, including the newly added line.
As you can see, the data is synchronized between originalfile.txt and hardlink.txt.

---

## 🗑️ Step 5: Delete the Original File

```bash
rm originalfile.txt

```

You might think the data is gone, right? Let’s check the hard link:

```bash
cat hardlink.txt

```
<img width="630" height="184" alt="image" src="https://github.com/user-attachments/assets/bdd9d075-476a-49f8-9aa5-89a8022d83e6" />

✅ Yes, it’s still there!
The data is safe because the hard link (hardlink.txt) still points to the same inode on disk — the actual data block.


Same for soft link.
