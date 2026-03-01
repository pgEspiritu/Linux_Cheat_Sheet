# 🔍 3. Search & Find

The `find` command is one of the most powerful Linux utilities.  
It allows you to search for files and directories based on **name, type, size, time, permissions, and more**.

---

## 🔹 Find Files

---

### 📌 1. `find / -name file.txt`

**Description:**  
Searches the entire system (`/`) for a file named `file.txt`.

**Example:**
```bash
find / -name file.txt
```

**Sample Output:**
```text
/home/user/Documents/file.txt
/var/www/html/file.txt
```

**Explanation:**

- / → Start searching from the root directory
- -name → Search by filename
- Case-sensitive search

#### 📌 Case-insensitive version:
```bash
find / -iname file.txt
```

**⚠️ Searching from / may require sudo:**
```bash
sudo find / -name file.txt
```

---

### 📌 2. find /var -type f -size +10M

**Description:**
Finds files larger than 10MB inside /var.

**Example:**
```bash
find /var -type f -size +10M
```

**Explanation:**
- `/var` → Starting directory
- `-type f` → Search only files
- `-size +10M` → Files larger than 10 Megabytes

**📌 Size Options:**

| Option | Meaning           |
| ------ | ----------------- |
| `+10M` | Greater than 10MB |
| `-10M` | Less than 10MB    |
| `10M`  | Exactly 10MB      |
| `k`    | Kilobytes         |
| `G`    | Gigabytes         |

Useful for disk cleanup and log analysis.

---

### 📌 3. find . -mtime -1

**Description:**
Finds files modified within the last 1 day in the current directory.

**Example:**
```bash
find . -mtime -1
```

Explanation:
- `.` → Current directory
- `-mtime` → Modified time (in days)
- `-1` → Less than 1 day ago (last 24 hours)

---

**📌 Time Variations:**

| Option       | Meaning                        |
| ------------ | ------------------------------ |
| `-mtime -7`  | Modified in last 7 days        |
| `-mtime +30` | Modified more than 30 days ago |
