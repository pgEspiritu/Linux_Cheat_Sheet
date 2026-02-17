## 🔹 Navigate Directories

Linux provides simple commands to **identify your current location** and **move between directories** in the filesystem.

---

### 📌 1. `pwd`
**Description:**  
Prints the **current working directory** (your exact location in the filesystem).

**Example:**
```bash
pwd
```

**Sample Output:**
```text
/home/user/Documents
```

#### Explanation:
- `pwd` stands for **Print Working Directory**
- Useful when you are unsure where you are in the directory tree
- Shows the full (absolute) path

---

### 📌 2. cd /home/user

**Description:**
Changes the directory to a specific absolute path.

**Example:**
```bash
cd /home/user
```

Verification:
```bash
pwd
```

**Sample Output:**
```text
/home/user
```

#### Explanation:
- `cd` stands for **Change Directory**
- /home/user is an absolute path (starts from root /)
- Use absolute paths to avoid confusion

---

### 📌 3. cd ..

**Description:**
Moves one level up to the parent directory.

**Example:**
```bash
cd ..
```

Scenario:
If your current directory is:
```text
/home/user/Documents
```

After running:
```bash
cd ..
```

You will be in:
```text
/home/user
```

#### Explanation:
- .. represents the parent directory
- Very useful for quick navigation upward

---

### 📌 4. cd ~

Description:
Navigates directly to the home directory of the current user.

**Example:**
```bash
cd ~
```

Sample Output (using pwd):
```text
/home/user
```

#### Explanation:
- `~` is a shortcut for the user's home directory
- Works regardless of your current location
- Faster than typing /home/username

---

### 📌 Pro Tip:
You can also go back to the previous directory using:
```bash
cd -
```

---

## ✅ Summary Table
| Command    | Purpose                      |
| ---------- | ---------------------------- |
| `pwd`      | Show current directory       |
| `cd /path` | Move to a specific directory |
| `cd ..`    | Move to parent directory     |
| `cd ~`     | Go to home directory         |
