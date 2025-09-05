# Permission Commands

## Reading Permissions

- In Linux, permissions are represented with a **10-character string**.  
- Permissions control what different owner types can do:  

**Permission Types**  
- **read (r)**:  
  - Files: read contents.  
  - Directories: list files/subdirectories.  
- **write (w)**:  
  - Files: modify contents.  
  - Directories: create files.  
- **execute (x)**:  
  - Files: run program.  
  - Directories: enter/access files.  

**Owner Types**  
- **user (u)**: file owner.  
- **group (g)**: group file owner belongs to.  
- **other (o)**: all other users.  

**Example: drwxrwxrwx**  
- 1st character = file type (`d` for directory, `-` for file).  
- Characters 2–4 = user permissions (rwx).  
- Characters 5–7 = group permissions (rwx).  
- Characters 8–10 = other permissions (rwx).  

---

## Exploring Existing Permissions

- `ls` → lists file names.  
- **Options**:  
  - `ls -a`: show hidden files.  
  - `ls -l`: show detailed permissions, owner, group, file size, last modified.  
  - `ls -la`: combine both.  

---

## Changing Permissions

### Principle of Least Privilege
- Grant only the **minimal access** needed to complete tasks.  
- Prevents unnecessary security risks.  

### `chmod` Command
- Syntax: `chmod <changes> <file>`  
- Example:  
  - `chmod u+rwx,g+rwx,o+rwx login_sessions.txt` → add all permissions.  
  - `chmod u-rwx,g-rwx,o-rwx login_sessions.txt` → remove all permissions.  
  - `chmod u=r,g=r,o=r login_sessions.txt` → assign only read permissions (overwrites others).  

### Symbols in `chmod`
- **u** = user  
- **g** = group  
- **o** = other  
- **+** = add permission  
- **-** = remove permission  
- **=** = set exact permissions  

👉 Separate multiple owner changes with commas, no spaces.  

---

## Example: Least Privilege in Action
- File: `bonuses.txt` in `/compensation` directory.  
- Owner: `hrrep1` (HR user).  
- Initial permissions: `-rw-rw----` (user = rw, group = rw, other = none).  
- Problem: HR group has unnecessary access.  
- Fix: `chmod g-rw bonuses.txt` → removes group read/write.  
- Result: Only `hrrep1` has access, aligning with least privilege.  

---

## Key Takeaways
- **Investigate permissions**: use `ls -l` or `ls -la`.  
- **Modify permissions**: use `chmod`.  
- **Principle of Least Privilege**: ensure only necessary users have required access.  
