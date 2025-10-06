### **IP Protocol Simplified (Cisco Terminology)**

**Purpose of IP:**

- IP (Internet Protocol) is a **connectionless, best-effort, media-independent protocol** that delivers packets from a source to a destination across networks.
- It is **lightweight (low overhead)**, providing only the functions necessary to move packets; it does **not track delivery or guarantee reliability**.

**Key Characteristics of IP:**

- **Connectionless:** No prior connection is established before sending data (like sending a letter without notifying the recipient).
- **Best Effort / Unreliable:** IP does **not guarantee packet delivery, ordering, or error correction**. Packets may arrive **late, out of order, corrupted, or not at all**. Reliability is handled by **TCP (Transport Layer, Layer 4)**.
- **Media Independent:** Works over any type of physical medium—copper, fiber, or wireless.

**How IP Works with the Data Link Layer (Layer 2):**

- The **Data Link Layer** prepares IP packets for transmission on the physical medium.
- It handles addressing via **MAC addresses** and ensures proper delivery within the local network (LAN).
- It informs the Network Layer (IP) of the **Maximum Transmission Unit (MTU)**—the largest packet that can travel over that medium.

**Fragmentation:**

- If an IP packet is **larger than the MTU** of the next network segment, a router splits it into smaller pieces called **fragments**.
- Fragmentation adds **latency**.
- **IPv4** supports router-based fragmentation; **IPv6** does **not**—packets must be sized before sending.

**Quick Cisco Terms to Know:**

- **IP Header:** Contains addressing and routing info.
- **PDU (Protocol Data Unit):** The packet at Layer 3 (IP packet).
- **MTU (Maximum Transmission Unit):** Maximum packet size the medium can carry.
- **Fragmentation:** Splitting IP packets for smaller MTUs.
- **Best Effort Delivery:** IP does not guarantee delivery.
- **Connectionless:** No session is established before sending packets.

**Summary Analogy:**

- IP = postal service: sends letters without guaranteeing delivery.
- TCP = tracking & confirmation: ensures letters arrive in order and intact.    
- Data Link Layer = local courier: delivers letters within the local neighborhood, knowing the exact house (MAC address).