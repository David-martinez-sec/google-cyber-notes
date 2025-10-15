# Filter Content in Linux

## Why Filtering Matters
- **Filtering** = selecting data that matches a condition (e.g., by file extension, text string, size, or modification time).  
- Useful for **security analysts** to quickly locate affected files (e.g., all `.txt` files targeted by malware).  

---

## `grep`
- **Purpose**: Searches for text patterns in files and returns matching lines.  
- Syntax: `grep <string> <file>`  

**Examples**  
- `grep OS updates.txt` → finds "OS" in updates.txt  
- `grep error time_logs.txt` → finds "error" in time_logs.txt  

---

## Piping (`|`)
- **Purpose**: Sends the output of one command into another as input.  
- Symbol: `|` (pipe). Often shares a key with `\` on keyboards.  

**Example**  
- `ls /home/analyst/reports | grep users`  
  - `ls` lists files in `reports`.  
  - Output is piped to `grep users`, which filters names containing "users".  

👉 **Note**: Piping is a general Linux redirection tool, not limited to filtering.  

---

## `find`
- **Purpose**: Search for files and directories based on criteria.  
- Syntax: `find <start_directory> <options>`  

### Options

#### `-name` vs `-iname`
- `-name`: case-sensitive.  
- `-iname`: case-insensitive.  

**Example**  
- `find /home/analyst/projects -name "*log*"`  
- `find /home/analyst/projects -iname "*log*"`  
- Finds files containing `"log"` in the name (`*` = wildcard for any characters).  

#### `-mtime`
- Search based on last modification in **days**.  

**Examples**  
- `find /home/analyst/projects -mtime -3` → modified in past 3 days  
- `find /home/analyst/projects -mtime +1` → modified more than 1 day ago  
- `find /home/analyst/projects -mtime -1` → modified within last 24 hours  

👉 Use `-mmin` instead of `-mtime` for minutes.  

---

## Key Takeaways
- Filtering commands make investigation faster and more precise.  
- **Key tools**:  
  - `grep` → search inside files.  
  - `|` (pipe) → chain commands and filter output.  
  - `find` → locate files by name, size, or modification time.  
