# Linux Architecture Explained

Understanding the Linux architecture is important for a security analyst. When you understand how a system is organized, it makes it easier to understand how it functions.  

A request to complete a task starts with the **user** and then flows through **applications**, the **shell**, the **Filesystem Hierarchy Standard (FHS)**, the **kernel**, and finally the **hardware**.  

---

## User
The **user** is the person interacting with a computer. They initiate and manage computer tasks.  
Linux is a **multi-user system**, meaning multiple users can access and share the same resources at the same time.  

---

## Applications
An **application** is a program that performs a specific task.  
- Some applications come **pre-installed** (e.g., calculator, calendar).  
- Others must be installed (e.g., web browsers, email clients).  

In Linux, applications are managed through a **package manager**:  
- A **package** is a piece of software that can be combined with other packages to form an application.  
- A **package manager** is a tool that helps install, manage, and remove packages.  

---

## Shell
The **shell** is the command-line interpreter.  
- It translates user commands into instructions the computer can execute.  
- Everything entered is **text-based**.  
- Think of it as the **translator** between the user and the computer.  

---

## Filesystem Hierarchy Standard (FHS)
The **FHS** organizes how data is stored and accessed in Linux.  
- A **directory** (also called a folder) organizes files and can contain files or other directories.  
- The FHS defines how directories, contents, and storage are structured so the OS knows where to find data.  

---

## Kernel
The **kernel** is the core of the Linux OS.  
- Manages **processes and memory**.  
- Communicates with applications to route commands.  
- Allocates resources across the system.  
- Controls all major functions of the **hardware**.  

The Linux kernel is unique to the Linux OS and is essential for system performance.  

---

## Hardware
The **hardware** includes all physical components of a computer. It is divided into **peripheral devices** and **internal hardware**.  

### Peripheral Devices
- Attached to and controlled by the computer system.  
- Not essential for core functionality.  
- Examples: **monitors, printers, keyboards, mice**.  

### Internal Hardware
- Required to run the system.  
- Built into the **motherboard**.  

Key components include:  
- **CPU (Central Processing Unit):** Executes program instructions and performs core computing tasks.  
- **RAM (Random Access Memory):** Short-term memory used for active tasks. Data is temporary and erased when power is off.  
- **Hard Drive:** Long-term storage for programs and files, accessible even after reboot.  

---

## Key Takeaways
- The Linux architecture is composed of:  
  **User → Applications → Shell → FHS → Kernel → Hardware**.  
- Each component plays a vital role in how Linux functions.  
- Security analysts benefit from understanding these components to better analyze, secure, and troubleshoot Linux systems.  
