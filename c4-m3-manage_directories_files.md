# Manage Directories and Files

## Creating and Modifying Directories

### `mkdir`
- Creates a new directory.  
- Works with **absolute** or **relative** paths.  
- Example:  
  - `mkdir /home/analyst/logs/network` → create new directory with absolute path.  
  - `mkdir network` (when already in `/home/analyst/logs`).  
- Pro Tip: Use `ls` to confirm directory creation.  

### `rmdir`
- Removes an **empty** directory.  
- Example: `rmdir /home/analyst/logs/network`.  
- Cannot delete directories that contain files/subdirectories.  

---

## Creating and Modifying Files

### `touch`
- Creates a new, empty file.  
- Example: `touch permissions.txt` (in `/home/analyst/reports`).  

### `rm`
- Deletes a file.  
- Example: `rm permissions.txt`.  
- ⚠️ Files deleted with `rm` are difficult to recover.  
- Pro Tip: Use `ls` to verify file changes.  

---

## Moving and Copying Files

### `mv`
- Moves a file or directory.  
- Example: `mv permissions.txt /home/analyst/logs`.  
- Can also **rename** files:  
  - `mv permissions.txt perm.txt`.  

### `cp`
- Copies a file or directory.  
- Example: `cp permissions.txt /home/analyst/logs`.  
- Copying keeps the original file in place.  

---

## `nano` Text Editor
- Command-line file editor (default in many Linux distributions).  
- Widely used by beginners and professionals.  

**Usage**  
- `nano permissions.txt` → opens file for editing.  
- `nano authorized_users.txt` → creates and opens a new file.  
- Save with `Ctrl + O`.  
- Exit with `Ctrl + X`.  
- Alternatives: **Vim** and **Emacs**.  

---

## Standard Output Redirection

- In addition to piping (`|`), you can redirect output using:  
  - `>` → overwrite file.  
  - `>>` → append to file.  

**Examples**  
- `echo "last updated date" >> permissions.txt` → append text.  
- `echo "time" > permissions.txt` → overwrite with new text.  

👉 Both operators create a new file if one does not already exist.  

---

## Key Takeaways
- **Directory management**: `mkdir`, `rmdir`.  
- **File management**: `touch`, `rm`, `mv`, `cp`.  
- **Editing**: `nano` (save with `Ctrl + O`, exit with `Ctrl + X`).  
- **Writing with redirection**: `>` (overwrite), `>>` (append).  
