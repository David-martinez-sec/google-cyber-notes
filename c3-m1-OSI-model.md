# Module 1 – The OSI Model

## Overview
The **Open Systems Interconnection (OSI) model** is a standardized conceptual framework with **seven layers**. It provides a more detailed view of how communication occurs across a network compared to the **TCP/IP model**.  
Security and network professionals use both models to:  
- Understand how data is transmitted.  
- Troubleshoot incidents.  
- Communicate about network processes and potential threats.  

---

## TCP/IP Model vs. OSI Model
- **TCP/IP Model**: 4 layers (Network Access, Internet, Transport, Application).  
- **OSI Model**: 7 layers (Application → Physical).  
- TCP/IP is a **simplified version** of OSI.  
- Both define standards and help analysts pinpoint where problems occur.  

---

## OSI Model Layers (Top-Down)

### Layer 7: Application Layer
- Directly involves the **user**.  
- Defines protocols applications use to connect to the internet.  
- Examples:  
  - **HTTP/HTTPS** → web browsing.  
  - **SMTP** → email.  
  - **DNS** → translates domain names to IP addresses.  
- Identifying feature: **user requests and responses**.  

---

### Layer 6: Presentation Layer
- Handles **data translation, formatting, and encryption**.  
- Ensures data is in a format usable by applications on both ends.  
- Functions:  
  - **Encryption** (e.g., SSL/TLS for HTTPS).  
  - **Compression** (reducing size for transfer).  
  - **Character code translation**.  

---

### Layer 5: Session Layer
- Manages **sessions** (connections) between devices.  
- Keeps sessions open during data transfer, terminates when complete.  
- Functions:  
  - Authentication.  
  - Reconnection after interruptions.  
  - **Checkpoints** → allow transfers to resume at the last saved point.  
- Bridges Presentation (L6) ↔ Transport (L4).  

---

### Layer 4: Transport Layer
- Ensures **end-to-end delivery** of data between devices.  
- Handles segmentation → breaks large transmissions into smaller **segments**.  
- Manages speed, flow, and reassembly of segments.  
- Protocols:  
  - **TCP**: Reliable, connection-oriented, retransmits errors.  
  - **UDP**: Fast, connectionless, used in real-time applications (e.g., streaming).  

---

### Layer 3: Network Layer
- Responsible for **packet delivery between networks**.  
- Uses **IP addresses** to determine destination.  
- Routers operate here.  
- Example protocol: **IP** (packets routed from source network → destination network).  

---

### Layer 2: Data Link Layer
- Organizes packet delivery **within a single network**.  
- Responsible for addressing devices via **MAC addresses**.  
- Switches and NICs operate here.  
- Protocols:  
  - **NCP** (Network Control Protocol).  
  - **HDLC** (High-Level Data Link Control).  
  - **SDLC** (Synchronous Data Link Control).  

---

### Layer 1: Physical Layer
- Deals with the **physical transmission medium**.  
- Hardware: hubs, modems, cables, wiring.  
- Converts packets into a stream of **0s and 1s** (binary signals).  
- Transmits across Ethernet or coaxial cables → passes signals up to higher layers.  

---

## Key Takeaways
- Both **TCP/IP** and **OSI** are conceptual models that describe data transmission.  
- **OSI** provides **seven communication layers**, with greater granularity.  
- Network and security professionals use OSI to:  
  - Identify potential issues at specific layers.  
  - Communicate disruptions and security threats effectively.  
- **TCP/IP** is widely used in practice, but **OSI remains an essential reference** for conceptualizing and teaching networking.  
