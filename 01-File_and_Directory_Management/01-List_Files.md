# 📂 1. File & Directory Management

## 🔹 List Files Using `ls`

The `ls` command is used to **list files and directories** in a Linux/Unix system.  
Different options (flags) modify how the output is displayed.

---

### 📌 1. `ls`
**Description:**  
Lists files and directories in the current directory.

**Example:**
```bash
ls
```

**Sample Output:**
```text
Documents  Downloads  notes.txt  script.py
```

#### Explanation:

- Displays names only
- No additional details
- Hidden files (starting with `.`) are not shown

---

### 📌 2. ls -l

**Description:**
Lists files in long format, showing detailed information.

**Example:**
```bash
ls -l
```

**Sample Output:**
```text
-rw-r--r-- 1 user user  1024 Feb 15 10:30 notes.txt
drwxr-xr-x 2 user user  4096 Feb 14 08:12 Documents
```

#### Explanation of Columns:

- `-rw-r--r--` → File permissions
- `1` → Number of links
- `user` → Owner
- `user` → Group
- `1024` → File size (bytes)
- `Feb 15 10:30` → Last modified date
- `notes.txt` → File name

---

### 📌 3. ls -la

**Description:**
Lists all files, including hidden files, in long format.

**Example:**
```bash
ls -la
```

**Sample Output:**
```text
drwxr-xr-x 3 user user 4096 Feb 15 09:00 .
drwxr-xr-x 5 user user 4096 Feb 14 08:00 ..
-rw-r--r-- 1 user user  220 Feb 10 07:45 .bashrc
-rw-r--r-- 1 user user 1024 Feb 15 10:30 notes.txt
```

**Explanation:**
- `.` → Current directory
- `..` → Parent directory
- Hidden files (starting with `.`) are now visible
- Useful for configuration and system checks

---

### 📌 4. ls -lh

**Description:**
Lists files in long format with human-readable file sizes.

**Example:**
```bash
ls -lh
```

**Sample Output:**
```text
-rw-r--r-- 1 user user 1.0K Feb 15 10:30 notes.txt
drwxr-xr-x 2 user user 4.0K Feb 14 08:12 Documents
```

#### Explanation:
- File sizes are shown in KB, MB, or GB
- Easier to read compared to raw byte values
- Ideal for checking storage usage quickly

---

### 📌 Tip:
You can combine options:
```bash
ls -lah
```

---

### ✅ Summary Table

| Command  | Purpose                                   |
| -------- | ----------------------------------------- |
| `ls`     | Basic file listing                        |
| `ls -l`  | Detailed (long) listing                   |
| `ls -la` | Detailed listing including hidden files   |
| `ls -lh` | Detailed listing with readable file sizes |
