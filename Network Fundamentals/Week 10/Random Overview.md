
# 📘 IPv6 Addressing & Key Concepts — Study Notes

---

## 1️⃣ **IPv6 Address Basics**

- **Length:** 128 bits
    
- **Format:** 8 groups of 4 hexadecimal digits (hextets), separated by colons  
    Example: `2001:0db8:0000:0000:00a0:0c2f:0000:0001`
    
- **Case-insensitive:** Can be written in uppercase or lowercase
    
- **Purpose:** Identifies devices and interfaces in IPv6 networks
    

---

## 2️⃣ **IPv6 Address Structure**

An IPv6 **unicast address** has two main components:

```
[Network Prefix | Subnet ID] : [Interface ID]
```

|Component|Meaning|Example|
|---|---|---|
|**Network Prefix**|Identifies the global network (like ISP-assigned network)|`2001:db8:acad`|
|**Subnet ID**|Identifies a specific subnet within the network|`:3:`|
|**Interface ID**|Identifies a specific interface/device in the subnet|`::1`|
|**Prefix Length**|Shows how many bits belong to network + subnet (usually /64)|`/64`|

**Example:**  
`2001:db8:acad:3::1/64`

- Network: `2001:db8:acad`
    
- Subnet ID: `3`
    
- Interface ID: `::1`
    

---

## 3️⃣ **Types of IPv6 Unicast Addresses**

|Type|Scope|Purpose|Example|
|---|---|---|---|
|**GUA (Global Unicast Address)**|Global|Internet communication; publicly routable|`2001:db8:acad:3::1/64`|
|**LLA (Link-Local Address)**|Local link only|Local communication, neighbor discovery, routing|`fe80::3:1`|

### 🔹 **Link-Local Address (LLA)**

- Always starts with `fe80::/10`
    
- **Automatically assigned** to every interface
    
- **Used for:**
    
    - Neighbor discovery
        
    - Routing protocols (e.g., OSPFv3, EIGRP for IPv6)
        
- **Not routable** beyond the local link
    

### 🔹 **Global Unicast Address (GUA)**

- Starts with `2000::/3`
    
- **Assigned by ISP or network admin**
    
- Used for **communication outside the local link / on the internet**
    

---

## 4️⃣ **IPv6 Network Segment**

- A **network segment** = all devices on the **same subnet or link** that can communicate **without a router**
    
- Devices in the **same segment** can reach each other directly
    
- Devices in a **different segment** need a **router** to communicate
    

**Example:**  
Subnet: `2001:db8:acad:3::/64`

- `2001:db8:acad:3::1` → Router interface
    
- `2001:db8:acad:3::2` → PC  
    ✅ Both can communicate directly (same segment)
    

---

## 5️⃣ **IPv6 vs IPv4**

|Feature|IPv6|IPv4|
|---|---|---|
|Local communication|Link-Local Address required (`fe80::/10`)|Optional (`169.254.x.x`)|
|Global communication|Global Unicast Address (`2000::/3`)|Public/private IP addresses|
|Broadcast|❌ No broadcast; uses multicast|✅ Broadcast exists|
|Interface requirement|✅ Every interface must have LLA|❌ Not required|

**Key Differences:**

- IPv6 uses **LLA for local link communication**, even if a GUA exists.
    
- IPv4 typically uses the same IP for local and global communication; link-local is optional.
    
- IPv6 **eliminates broadcast**, using **multicast and link-local** addresses instead.
    

---

## 6️⃣ **Example Router Configuration**

```bash
R1(config)#interface s0/1/0
R1(config-if)#ipv6 address fe80::3:1 link-local
R1(config-if)#ipv6 address 2001:db8:acad:3::1/64
R1(config-if)#no shutdown
```

- `fe80::3:1` → **Link-Local Address** for local link communication
    
- `2001:db8:acad:3::1/64` → **Global Unicast Address** for internet/global reachability
    
- `no shutdown` → Activates the interface
    

---

### ✅ **Summary Tips**

1. **Every IPv6 interface must have an LLA** for local operations.
    
2. **GUA is optional** but required for internet/global communication.
    
3. **Subnet ID** organizes large networks into smaller segments.
    
4. **Interface ID** uniquely identifies the device in the subnet.
    
5. **Network segment** = devices on the same subnet/link that can communicate directly.
    

---

If you want, I can also **add a small diagram showing LLA vs GUA vs subnet/interface IDs on a router and PCs**, which makes this super easy to visualize for studying.

Do you want me to do that?