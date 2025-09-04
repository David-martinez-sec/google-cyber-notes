# Navigate Linux and Read File Content

## Filesystem Hierarchy Standard (FHS)

- **FHS** organizes data in Linux: defines how directories, contents, and storage are structured.
- A **file path** describes a file’s location. Paths use `/` to separate hierarchy levels.
- **Root directory `/`**  
  - Highest-level directory.  
  - All other directories branch from root.  

### Standard FHS Directories
- `/home`: User-specific home directories.
- `/bin`: "Binary" – executables and programs.
- `/etc`: System configuration files.
- `/tmp`: Temporary files (commonly targeted by attackers).
- `/mnt`: "Mount" – external media like USB drives or disks.

👉 Use `man hier` for more details about FHS.

### User-Specific Subdirectories
- Each user under `/home` has personal directories (e.g., `/home/analyst/logs`).
- Shortcuts:
  - `~` = user’s home directory (e.g., `~/logs`).
  - `.` = current directory.
  - `..` = parent directory.
- **Absolute path**: full path from `/` (e.g., `/home/analyst/projects`).  
- **Relative path**: based on current location (e.g., `../projects`).

---

## Key Navigation Commands

### `pwd`
- Prints working directory (absolute path).
- Example: `/home/analyst`.
- Pro Tip: Use `whoami` to confirm current user.

### `ls`
- Lists files and directories.
- Add path to see contents elsewhere:  
  - `ls projects` or `ls /home/analyst/projects`.

### `cd`
- Changes directory.  
  - `cd projects` → move into subdirectory.  
  - `cd /home/analyst/logs` → absolute path.  
  - `cd ..` → move up one level.

---

## Commands for Reading File Content

### `cat`
- Displays entire file.  
  - Example: `cat updates.txt`.

### `head`
- Displays first 10 lines by default.  
  - Example: `head updates.txt`.  
- Adjust line count:  
  - `head -n 5 updates.txt`.

### `tail`
- Displays last 10 lines by default.  
  - Example: `tail updates.txt`.  
- Useful for viewing **latest log entries**.

### `less`
- Views file one page at a time.  
  - Example: `less updates.txt`.  
- Navigation inside `less`:  
  - `Space`: forward one page.  
  - `b`: back one page.  
  - `↓` / `↑`: line-by-line.  
  - `q`: quit.

---

## Key Takeaways
- **Navigation commands**: `pwd`, `ls`, `cd`.
- **File reading commands**: `cat`, `head`, `tail`, `less`.
- Being fluent with Linux navigation and file reading is essential for **security analysts**, especially when working with logs and system files.
