# Packets and Frames

## Packets
- Small pieces of data from **Layer 3 (Network Layer)**  
- Contain:
  - **IP header**
  - **Payload**

## Frames
- Used at **Layer 2 (Data Link Layer)**  
- Encapsulate packets, containing **MAC address**  
- **Analogy:** Frame = Envelope, Packet = Letter inside  

---

## Why Packets Are Used?
- Efficient way of communicating data across networks.  
- Small pieces reduce chance of **bottlenecks**.  
- Packets using IP contain:
  - **Time to Live (TTL):** expiry timer for a packet  
  - **Checksum:** integrity checking protocol for TCP/IP  
  - **Source IP address**  
  - **Destination IP address**  

---

# TCP/IP (Transmission Control Protocol / Internet Protocol)

- **TCP/IP** = Model  
- **TCP** = Protocol  
- Similar to OSI model but has **4 layers**:  
  1. **Application Layer** → (Application + Session + Presentation)  
  2. **Transport Layer**  
  3. **Network Layer** → (Network + Data Link)  
  4. **Physical Layer**

### Key Concepts
- **Encapsulation/Decapsulation:** Information is added/stripped off at each layer.  
- **TCP is connection-based** → must establish a connection first.  
- **Guarantees delivery & integrity of data.**

---

## TCP

### Advantages
- Ensures **integrity** of data.  
- Synchronizes devices to prevent flooding.  
- Provides **reliability**.  

### Disadvantages
- Requires a **reliable connection**.  
- Slower than UDP.  
- Holds up network if connection is weak.  

### TCP Packet Contains
- Source Port  
- Destination Port  
- Source IP  
- Destination IP  
- Sequence Number (first piece of info given random number)  
- ACK Number (Sequence Number + 1)  
- Checksum  
- Data  
- Flag (how packet should be handled)  

---

## 3-Way Handshake
1. **SYN** → Client initiates connection.  
2. **SYN/ACK** → Server acknowledges sync attempt.  
3. **ACK** → Client confirms sync.  
4. **DATA** → Connection established, data transfer begins.  
5. **FIN** → Cleanly close connection.  
6. **RST** → Abruptly end connection if error occurs.  

### Example Sequence
- SYN (Client → ISN = 0)  
- SYN/ACK (Server → ISN = 5000, ACK = 0)  
- ACK (Client → ACK = 5000, ISN = 1)  

---

## Closing a TCP Connection
- Client sends **FIN** → Server ACKs.  
- Server sends **FIN** → Client ACKs.  

---

# UDP (User Datagram Protocol)

- **Stateless** → No 3-way handshake.  
- No synchronization between devices.  

### Advantages
- **Faster** than TCP.  
- No constant reserved connection.  
- Allows apps to control packet sending speed.  

### Disadvantages
- No guarantee data will be received.  
- Bad on unstable connections.  

### UDP Header Contains
- Time to Live  
- Source Address  
- Destination Address  
- Source Port  
- Destination Port  
- Data  

---

# Ports

- Ports = communication endpoints.  
- **Analogy:** Like a ship docking at a port — must fit the rules of that port.  
- Once a connection is established, data is sent/received via specific ports.  
- Range: **0 – 65535**  

### Common Ports
- **21** → FTP (File Transfer Protocol)  
- **22** → SSH (Secure Shell)  
- **80** → HTTP (HyperText Transfer Protocol)  
- **443** → HTTPS (HyperText Transfer Protocol Secure)  
- **445** → SMB (Server Message Block)  
- **3389** → RDP (Remote Desktop Protocol)  


