# Networking Concepts

## Port Forwarding
- **Definition:** Enables external (Internet) access to internal services.
- Without port forwarding, services like web servers are only reachable by devices on the same **local network** (intranet).
- Forwarding through the router allows devices on another network to access internal services using the **public IP**.
- Example rule:  
  *If someone connects to my public IP on port X, forward that traffic to my private IP on port X (or another port I specify).*

---

## Firewalls
- **Function:** Determines what traffic is allowed to enter or exit a network.  
- Firewalls can filter based on:
  - **Source** (where traffic is coming from)  
  - **Destination** (where traffic is going to)  
  - **Port** (e.g., port 80, 443, 22)  
  - **Protocol** (TCP, UDP, etc.)  
- Packet inspection is used to enforce rules.  
- Firewalls can be:
  - **Hardware** (dedicated device)  
  - **Software** (like Snort, pfSense)

### Types of Firewalls
- **Stateful:**
  - Dynamic decision-making.
  - Considers the entire connection.
  - More resource-heavy.
  - If connection is bad, the whole device can be blocked.  

- **Stateless:**
  - Uses static rules (packet-by-packet).
  - Less resource intensive.
  - Great for **large traffic volumes** (e.g., mitigating DDoS attacks).
  - Less flexible if rules don’t exactly match.

---

## Virtual Private Network (VPN)
- **Definition:** Allows two devices on different networks to communicate by creating a **dedicated private tunnel**.
- Benefits:
  - Privacy → Encryption ensures only intended devices can read data.  
  - Anonymity → Masks your IP with the server’s IP.  
  - Geo-connectivity → Connect networks in different geographical locations.  
- Notes:
  - ISPs can see you’re connected to a VPN but cannot see the data inside the tunnel.  
  - **Log VPNs** may store your data → risk of leaks.  
  - **No-log VPNs** offer stronger anonymity.  

### VPN Technologies
- **PPP (Point-to-Point Protocol):**
  - Used by PPTP for authentication & encryption.
  - Requires matching public certificate & private key.
  - Non-routable.  

- **PPTP (Point-to-Point Tunneling Protocol):**
  - Wraps PPP traffic to travel outside the network.
  - Easy to set up, but weakly encrypted.  

- **IPSec (Internet Protocol Security):**
  - Uses IP framework to encrypt traffic.
  - Harder to configure but very secure.  

