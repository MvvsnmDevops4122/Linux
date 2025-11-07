
# awk: A Powerful Text Processing Command in Linux
=================================================

The `awk` command is used to **process text data**, especially when data is arranged in **columns**.  
It reads input line-by-line and allows filtering, extracting, and formatting of data.

---

## 📌 Examples Using `employees.txt`

```bash
John   35   50000   john@example.com
Alice  42   62000   alice@example.com
Bob    28   40000   bob@example.com
Nina   50   75000   nina@example.com
Sam    38   46000   sam@example.com
Priya  29   52000   priya@example.com
Boult  43   45000   boult@example.com
```

### Display the complete data
```

awk '{print}' employees.txt
awk '{print $0}' employees.txt

```

### Display all lines that contain the word "Bob"
```

awk '/Bob/' employees.txt

```

### Display the 1st and 3rd columns
```

awk '{print $1, $3}' employees.txt

```

### Display the 1st and last columns (`$NF` = last field)
```

awk '{print $1, $NF}' employees.txt

```

### Display columns in reverse order
```

awk '{print $4, $3, $2, $1}' employees.txt

```

### Display data along with row number (`NR`)
```

awk '{print NR, $0}' employees.txt

```

---

## 🎯 Conditional Filtering

### Display records where age is **less than 40**
```

awk '$2 < 40 {print}' employees.txt

```

### Display records where age is **between 30 and 40**
```

awk '$2 >= 30 && $2 <= 40 {print NR, $0}' employees.txt

```

### Display records where salary is **greater than 50,000**
```

awk '$3 > 50000' employees.txt

```

---

## 📜 Print Specific Line Range

### Print lines 10 to 20 from a file
```

awk 'NR >= 10 && NR <= 20' file.txt
awk 'NR >= 10 && NR <= 20 {print}' file.txt

```

---

## 🔧 Useful Related Commands

### Download a file from the internet
```

wget <URL>

```

### Save output to a file while displaying it on screen
```

command | tee output.txt

```
**Example:**
```

script.sh | tee output.txt

```

### Remove **consecutive** duplicate lines
```

uniq filename

```

> To remove duplicates completely (not only consecutive):
```

sort filename | uniq

```

---

## ✅ Summary
- `awk` is best for **column-wise text processing**
- `$1`, `$2`, `$NF` → Access specific fields
- `NR` → Row/line number
- Supports filtering, searching & formatting


