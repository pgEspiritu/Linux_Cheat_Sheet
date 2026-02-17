## 🔹 Copy, Move, and Delete Files & Directories

Linux provides powerful commands to **copy**, **rename/move**, and **delete** files and directories.  
⚠️ Be careful—some delete operations are **permanent** and cannot be undone.

---

## 📌 Copy Files & Directories

### 1. `cp file1 file2`
**Description:**  
Copies a file to another file or name.

**Example:**
```bash
cp file1.txt file2.txt
```

#### Explanation:
- Creates file2.txt as a copy of file1.txt
- If file2.txt exists, it will be overwritten (no warning by default)

**Tip (safer copy):**
```bash
cp -i file1.txt file2.txt
```
Prompts before overwriting.

---

### 2. cp -r dir1 dir2

**Description:**
Copies a directory recursively (including all contents).

**Example:**
```bash
cp -r projects backup_projects
```

#### Explanation:
- `-r` means recursive
- Copies files and subdirectories inside dir1
- Required when copying directories

---

### 📌 Move & Rename Files
3. mv oldname newname

**Description:**
Renames a file or directory.

**Example:**
```bash
mv oldname.txt newname.txt
```

#### Explanation:
- Same command used for renaming
- No copy is made; the name is changed directly

---

### 4. mv file /path/

**Description:**
Moves a file to another directory.

**Example:**
```bash
mv report.pdf /home/user/Documents/
```

#### Explanation:
- Moves the file to the specified location
- Keeps the same filename unless changed

---

### 📌 Delete Files & Directories
5. rm file

**Description:**
Deletes a file.

**Example:**
```bash
rm notes.txt
```

#### Explanation:
- Permanently deletes the file
- No recycle bin in the terminal ❌

---

### 6. rm -r folder

**Description:**
Deletes a directory and its contents recursively.

**Example:**
```bash
rm -r old_folder
```

#### Explanation:
- Required for deleting directories
- Prompts may appear if files are write-protected

---

### 7. rm -rf folder ⚠️ DANGEROUS

**Description:**
Forcefully deletes a directory and all contents without confirmation.

Example:
```bash
rm -rf temp_folder
```

#### Explanation:
- `-r` → recursive
- `-f` → force (no prompts, ignore errors)
- Very dangerous if used incorrectly

🚨 WARNING:
```bash
rm -rf /
```
This can destroy an entire system.

---

### 📌 Safety Tips:

- Always double-check paths before using rm -rf
- Use ls before deleting:
  ```bash
  ls folder
  ```
  - Use interactive mode for safety:
  ```bash
  rm -ri folder
  ```

---

### ✅ Summary Table
| Command           | Purpose                  |
| ----------------- | ------------------------ |
| `cp file1 file2`  | Copy a file              |
| `cp -r dir1 dir2` | Copy a directory         |
| `mv old new`      | Rename a file/directory  |
| `mv file /path/`  | Move a file              |
| `rm file`         | Delete a file            |
| `rm -r folder`    | Delete a directory       |
| `rm -rf folder`   | Force delete (dangerous) |

