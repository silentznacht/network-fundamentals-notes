
A logical AND is one of three Boolean operations used in Boolean or digital logic. The other two are OR and NOT. The AND operation is used in determining the network address.

Logical AND is the comparison of two bits that produce the results shown below. Note how only a 1 AND 1 produces a 1. Any other combination results in a 0.

Exmp 
- 1 AND 1 = 1
- 0 AND 1 = 0
- 1 AND 0 = 0
- 0 AND 0 = 0

**Note:** In digital logic, 1 represents True and 0 represents False. When using an AND operation, both input values must be True (1) for the result to be True (1).

To identify the network address of an IPv4 host, the IPv4 address is logically ANDed, bit by bit, with the subnet mask. ANDing between the address and the subnet mask yields the network address.

To illustrate how AND is used to discover a network address, consider a host with IPv4 address 192.168.10.10 and subnet mask of 255.255.255.0, as shown in the figure:
- **IPv4 host address (192.168.10.10)** - The IPv4 address of the host in dotted decimal and binary formats.
- **Subnet mask (255.255.255.0)** - The subnet mask of the host in dotted decimal and binary formats.
- **Network address (192.168.10.0)** - The logical AND operation between the IPv4 address and subnet mask results in an IPv4 network address shown in dotted decimal and binary formats.
![[Pasted image 20251011192942.png]]

Note: This primarily done for routers, so that a router can repersent and entire subnet, that can communicate with a main router that communicates with all other subnets.

Here’s a **concise, study-note version** of what you wrote, keeping it clear, technical, and exam-friendly:

---

## **Logical AND and Determining Network Addresses**

### **1. Logical AND in Digital Logic**

- One of three Boolean operations: **AND, OR, NOT**.
    
- **AND operation:**
    
    - `1 AND 1 = 1`
        
    - `1 AND 0 = 0`
        
    - `0 AND 1 = 0`
        
    - `0 AND 0 = 0`
        
- **Note:** `1 = True`, `0 = False`. Both inputs must be `1` for the result to be `1`.
    

---

### **2. Using AND to Find a Network Address**

- **Purpose:** Identify the **network portion** of an IP address.
- **Process:**
    
    1. Convert IP address and subnet mask to binary.
        
    2. Perform **bitwise AND** between each corresponding bit.
        
    3. Result = **network address**, representing the whole subnet.
        

**Example:**

```
IP Address:       192.168.10.10 → 11000000.10101000.00001010.00001010
Subnet Mask:      255.255.255.0 → 11111111.11111111.11111111.00000000
Network Address:  192.168.10.0 → 11000000.10101000.00001010.00000000
```

- **IP Address** → unique to the host
    
- **Network Address** → shared by all devices on that subnet
    

---

### **3. Why It Matters**

- **Hosts** use the network address to know whether traffic is **local or needs routing**.
    
- **Routers** use the network address to **represent an entire subnet** and route traffic between subnets.
    

> 💡 **Key Concept:** ANDing locks the network portion (via subnet mask) and isolates the host portion, allowing routers to manage traffic efficiently across multiple subnets.