## 🔹 Create Files & Directories

Linux provides simple commands to **create empty files** and **create directories**, including nested directory structures.

---

### 📌 1. `touch file.txt`
**Description:**  
Creates an **empty file** or updates the timestamp of an existing file.

**Example:**
```bash
touch file.txt
```

Verification:
```bash
ls
```

**Sample Output:**
```text
file.txt
```

#### Explanation:

- If file.txt does not exist, it will be created
- If it already exists, its last modified time is updated
- Commonly used to quickly create placeholder files

---

### 📌 2. mkdir folder

**Description:**
Creates a single directory.

**Example:**
```bash
mkdir folder
```

Verification:
```bash
ls
```

**Sample Output:**
```text
folder
```

#### Explanation:
- `mkdir` stands for Make Directory
- Fails if the directory already exists (unless -p is used)
- Ideal for organizing files into folders

---

### 📌 3. mkdir -p parent/child

**Description:**
Creates parent and child directories in one command.

**Example:**
```bash
mkdir -p parent/child
```

Verification:
```bash
tree parent
```

Sample Output:
```text
parent
└── child
```

#### Explanation:
- `-p` means parents
- Automatically creates missing directories
- No error if directories already exist
- Very useful for scripts and automation

---

### 📌 Pro Tips:

- Create multiple files at once:
```bash
touch a.txt b.txt c.txt
```

- Create multiple directories:
```bash
mkdir dir1 dir2 dir3
```

- Create deep structures safely:
```bash
mkdir -p project/{src,docs,tests}
```

---

### ✅ Summary Table
| Command                 | Purpose                   |
| ----------------------- | ------------------------- |
| `touch file.txt`        | Create an empty file      |
| `mkdir folder`          | Create a directory        |
| `mkdir -p parent/child` | Create nested directories |
