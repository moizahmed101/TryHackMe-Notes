# Introduction to LAN  

## 🌐 What is a LAN?  
- **LAN (Local Area Network)** is a network of devices within a limited area (home, office, school).  
- Helps devices communicate and share resources like files, printers, and internet.  

---

## 🔗 Network Topologies  

### ⭐ Star Topology (Most Common)  
- Devices connect individually via a central device (**Switch/Hub**).  
- **Reliability:** Medium – devices independent, but if central device fails, whole network fails.  
- **Security:** Medium – central device is a single point of attack.  
- **Cost:** High – requires more cables and a switch.  
- **Expansion:** Easy – new devices can be added quickly.  
- **Speed:** High.  
- **Maintenance:** Medium – easy at first, harder with scale.  

---

### 🚌 Bus Topology  
- All devices connect to a **single backbone cable**.  
- **Reliability:** Low – if backbone fails, entire system goes down.  
- **Security:** Weak – shared line, easy to intercept.  
- **Cost:** Very low – minimal cabling, no extra devices.  
- **Expansion:** Limited – adding devices increases collisions.  
- **Speed:** Decreases with more devices.  
- **Maintenance:** Gets difficult as network grows.  

---

### 🔄 Ring Topology  
- Devices form a **circular path**; data moves one way (or both in dual ring).  
- **Reliability:** Low – single cut/device failure stops whole network.  
- **Security:** Very low – data passes through multiple devices.  
- **Cost:** Low – less cabling, may require repeater.  
- **Expansion:** Hard – adding/removing breaks ring.  
- **Speed:** Slower than star/mesh.  
- **Maintenance:** Easier to troubleshoot.  

---

### 🔗 Mesh Topology  
- Each device directly connects to every other device.  
- **Reliability:** Very high – no single point of failure.  
- **Security:** Very high – dedicated connections, no shared data.  
- **Cost:** Very high – huge cabling requirements.  
- **Expansion:** Difficult – complexity grows with devices.  
- **Speed:** Very fast – no bottlenecks.  
- **Maintenance:** Hard – too many cables to manage.  

---

## 🖥 Networking Devices  

### 🔀 Switch  
- Connects multiple devices in a LAN.  
- Works at **Data Link Layer (Layer 2)**.  
- Uses **MAC addresses** to forward data efficiently.  
- Only sends data to the intended target (unlike a hub).  

### 📡 Router  
- Connects **different networks** (e.g., Home LAN ↔ Internet).  
- Works at **Network Layer (Layer 3)**.  
- Uses **IP addresses** for routing.  
- Functions:  
  - **NAT** (Network Address Translation) → allows private IPs to access the internet.  
  - **DHCP** (assigns IPs), **VPN**, **Firewall** features.  

### 🔌 Hub  
- Broadcasts data to all devices (no intelligence).  
- Works at **Layer 1 (Physical layer)**.  
- Cheaper but inefficient compared to switches.  

---

## 🧩 VLAN (Virtual LAN)  
- Divides one physical network into multiple **logical networks**.  
- **Security:** Devices in different VLANs cannot talk unless rules allow.  
- **Organization:** Group devices by departments/roles.  
- **Efficiency:** Reduces unnecessary traffic (devices only talk within their VLAN).  

