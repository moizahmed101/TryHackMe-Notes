# OSI Model

**Open System Interconnection (OSI) Model**  
The OSI model is a framework dictating how all network devices send, receive, and interpret data.  
It ensures that devices with different designs and functions can still communicate across networks.  

The model is divided into **7 layers**:

1. Physical Layer (1)  
2. Data Link Layer (2)  
3. Network Layer (3)  
4. Transport Layer (4)  
5. Session Layer (5)  
6. Presentation Layer (6)  
7. Application Layer (7)  

---

## Encapsulation
- At each layer, data is processed and extra information is added (called **headers** and **trailers**).  
- Each layer adds a header, except the **Physical Layer**.  
- **Data Link Layer** adds both a header and trailer.  

---

## Layer Details

### 1. Physical Layer (Layer 1)
- Defines the interface between devices and the transmission medium.  
- Data here is raw bits (`0` and `1`) converted into electrical/optical/radio signals.  
- Determines: topology, line configuration, transmission medium, data rate synchronization.  

---

### 2. Data Link Layer (Layer 2)
- Converts raw bit stream into **frames** (and vice versa).  
- Uses **MAC addresses** for physical addressing.  
- Adds headers with MAC address of recipient device.  
- Example device: **NIC (Network Interface Card)**.  

---

### 3. Network Layer (Layer 3)
- Responsible for **logical addressing** using **IP addresses**.  
- Converts frames → packets.  
- Handles routing with protocols like **OSPF** and **RIP**.  
- Chooses path based on: reliability, shortest path, and link type (copper/fiber).  

---

### 4. Transport Layer (Layer 4)
Two main protocols:  

#### TCP (Transmission Control Protocol)
- Reliable, connection-oriented.  
- Ensures error-checking, data order, and synchronization.  
- Advantages: accurate, reliable.  
- Disadvantages: slower, resource-heavy.  
- Used in: file sharing, web browsing, email.  

#### UDP (User Datagram Protocol)
- Unreliable, connectionless.  
- Faster, no error-checking, no guarantee of delivery.  
- Used in: streaming, online games, VoIP.  

---

### 5. Session Layer (Layer 5)
- Establishes, maintains, and terminates sessions between applications.  
- Adds checkpoints for recovery if connection breaks.  
- Manages dialog control (half-duplex/full-duplex).  

---

### 6. Presentation Layer (Layer 6)
- Translation between app data and standard format.  
- Handles: encoding (ASCII, Unicode), format conversion (JPEG, MP3, MPEG).  
- Encryption/Decryption (SSL/TLS).  
- Compression (ZIP, JPEG).  

---

### 7. Application Layer (Layer 7)
- Closest to users, where apps operate.  
- Provides services: file transfer, email, directory services, web browsing.  
- Protocols include:  
  - **HTTP/HTTPS** → web browsing  
  - **SMTP, POP3, IMAP** → email  
  - **FTP** → file transfer  
  - **DNS** → domain name resolution  
  - **SSH/Telnet** → remote login  

---
