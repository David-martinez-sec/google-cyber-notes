# Responsible Use of sudo

## Why sudo Matters
- Running as the **root user** is risky:
  - Difficult to track who ran commands.
  - Easy to make irreversible mistakes.
  - If compromised, attackers gain full control.
- Instead, use **sudo**:
  - Temporarily grants elevated privileges.
  - Defined in the **sudoers file** (which users can use sudo).
  - Safer than logging in as root, but still carries risks.

**Analogy**: Like a hotel master key — useful for staff, but dangerous if stolen.  
👉 Only grant sudo to those who truly need it.

---

## Authentication vs Authorization
- **Authentication**: verifying identity (who someone is).  
- **Authorization**: granting access (what they can do).  
- sudo helps manage **authorization tasks** securely.  

---

## Key Commands with sudo

### `useradd`
- Adds a new user.  
- Example: `sudo useradd fgarcia`  
- Options:  
  - `-g` → set primary group  
    - `sudo useradd -g security fgarcia`  
  - `-G` → add supplemental (secondary) groups  
    - `sudo useradd -G finance,admin fgarcia`  

---

### `usermod`
- Modifies an existing user.  
- Options:  
  - `-g` → change primary group  
    - `sudo usermod -g executive fgarcia`  
  - `-G` → change supplemental groups (⚠️ replaces groups)  
  - `-a -G` → append supplemental groups (preferred)  
    - `sudo usermod -a -G marketing fgarcia`  

Other useful options:  
- `-d` → change home directory  
  - `sudo usermod -d /home/garcia_f fgarcia`  
- `-l` → change login name  
- `-L` → lock account (prevent login)  

---

### `userdel`
- Deletes a user.  
- Example: `sudo userdel fgarcia`  
- `-r` → also delete home directory and files.  
  - `sudo userdel -r fgarcia`  

👉 Safer alternative: lock account instead of deleting.  
- `sudo usermod -L fgarcia` → user can’t log in, but files remain accessible.  

---

### `chown`
- Changes file/directory ownership.  
- Example:  
  - `sudo chown fgarcia access.txt` → change user owner.  
  - `sudo chown :security access.txt` → change group owner.  
- Options available for more complex ownership changes.  

---

## Key Takeaways
- Use **sudo** for elevated privileges instead of logging in as root.  
- **Authentication** = who you are. **Authorization** = what you can do.  
- Manage users and ownership with:  
  - `useradd` → add users.  
  - `usermod` → modify accounts (groups, home dir, login, lock).  
  - `userdel` → delete users (or lock accounts for safety).  
  - `chown` → change file/directory ownership.  
