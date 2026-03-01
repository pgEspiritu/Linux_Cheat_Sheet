## 🔹 Text Editors in Linux

Linux provides built-in terminal-based text editors.  
They are useful for editing configuration files, scripts, and logs directly from the CLI.

---

### 📌 1. `nano file.txt`
**Description:**  
A **simple and beginner-friendly** text editor.

**Example:**
```bash
nano file.txt
```

**What Happens:**
- Opens file.txt in the Nano editor
- If the file does not exist, it creates a new one

Common Shortcuts (shown at bottom of screen):
| Shortcut   | Action     |
| ---------- | ---------- |
| `Ctrl + O` | Save file  |
| `Ctrl + X` | Exit       |
| `Ctrl + K` | Cut line   |
| `Ctrl + U` | Paste line |
| `Ctrl + W` | Search     |

**Why Use Nano?**
- Easy to learn
- Commands displayed on-screen
- Ideal for beginners

---

### 📌 2. vim file.txt

**Description:**
An advanced and powerful text editor (improved version of vi).

**Example:**
```bash
vim file.txt
```

**Modes in Vim:**
```bash
| Mode         | Purpose               |
| ------------ | --------------------- |
| Normal Mode  | Navigation & commands |
| Insert Mode  | Typing text           |
| Command Mode | Saving & quitting     |
```

**Basic Workflow:**
1. Press i → Enter Insert Mode
2. Type your text
3. Press Esc → Return to Normal Mode
4. Type :wq → Save and Quit

**Other Useful Commands:**
```bash
:w      # Save
:q      # Quit
:q!     # Quit without saving
```

**Why Use Vim?**
- Extremely powerful
- Fast navigation
- Popular in DevOps & server environments

---

### 📌 3. vi file.txt

**Description:**
The original Unix text editor (basic version of Vim).

**Example:**
```bash
vi file.txt
```

**Explanation:**
- Works similarly to Vim
- Available on almost all Unix/Linux systems
- Fewer features compared to Vim

---

### ✅ Comparison Table

| Editor | Difficulty   | Best For               |
| ------ | ------------ | ---------------------- |
| `nano` | ⭐ Easy       | Beginners              |
| `vim`  | ⭐⭐⭐ Advanced | Developers / SysAdmins |
| `vi`   | ⭐⭐ Moderate  | Minimal systems        |

---

### 📌 Pro Tip:
If you're managing remote Linux servers (like EC2 instances), learning vim is highly recommended — especially for editing config files such as:
```bash
/etc/nginx/nginx.conf
/etc/ssh/sshd_config
```
It’s a must-have skill for DevOps and system administration 🚀
