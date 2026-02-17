# 📄 2. Viewing & Editing Files

Linux provides several commands to **view file contents** without opening a graphical editor.  
These tools are essential for inspecting logs, configuration files, and text files.

---

## 🔹 View File Contents

### 📌 1. `cat file.txt`
**Description:**  
Displays the **entire contents** of a file at once.

**Example:**
```bash
cat file.txt
```

**Sample Output:**
```text
Line 1
Line 2
Line 3
```

#### Explanation:
- cat stands for concatenate
- Best for small files
- Output scrolls directly to the terminal
⚠️ Not ideal for large files (content scrolls too fast)

---

### 📌 2. less file.txt

**Description:**
Views file contents page by page with navigation.

**Example:**
```bash
less file.txt
```
Navigation Keys:
- Space → Next page
- b → Previous page
- /word → Search
- q → Quit

#### Explanation:
- Handles large files efficiently
- Most commonly used file viewer

---

### 📌 3. more file.txt

**Description:**
Displays file contents one screen at a time.

**Example:**
```bash
more file.txt
```

#### Explanation:
- Older and simpler than less
- Limited navigation (mostly forward only)
- Press `Space` to continue

---

### 📌 4. head file.txt

**Description:**
Displays the first 10 lines of a file.

**Example:**
```bash
head file.txt
```

**Custom Lines Example:**
```bash
head -n 5 file.txt
```

#### Explanation:
- Useful for quickly checking file headers
- `-n` specifies number of lines

---

### 📌 5. tail file.txt

**Description:**
Displays the last 10 lines of a file.

**Example:**
```bash
tail file.txt
```

**Custom Lines Example:**
```bash
tail -n 20 file.txt
```

#### Explanation:
- Commonly used for logs
- Helps inspect recent entries

---

### 📌 6. tail -f logfile.log

**Description:**
Continuously displays new lines as the file grows.

**Example:**
```bash
tail -f logfile.log
```

#### Explanation:
- `-f` means follow
- Ideal for real-time log monitoring
- Press `Ctrl + C` to stop

---

### 📌 Pro Tip:
Combine commands with pipes:
```bash
ps aux | head
```
This shows only the first few lines of a long output ✔️

---

### ✅ Summary Table
| Command         | Purpose             |
| --------------- | ------------------- |
| `cat file.txt`  | View entire file    |
| `less file.txt` | Scroll through file |
| `more file.txt` | Simple paged view   |
| `head file.txt` | View first lines    |
| `tail file.txt` | View last lines     |
| `tail -f file`  | Live log monitoring |
