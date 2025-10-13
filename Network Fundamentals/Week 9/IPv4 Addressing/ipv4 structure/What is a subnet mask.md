A **subnet mask** is a **32-bit number** that tells the computer which part of an IP address is the **network portion** and which part is the **host portion**.
- **Network portion:** Identifies which subnet the device belongs to.
- **Host portion:** Identifies the specific device within that subnet.

**📘 Study Note: Subnet Masks (Simplified but Technical Explanation)**
### 🧠 What a Subnet Mask Does

A **subnet mask** tells computers **which part of an IP address belongs to the network**and **which part belongs to the host** (individual device).

It’s like saying:

> “These bits must stay the same for everyone in this network — but the rest can vary for each device.”

---

### 🔢 Example

**IP Address:** 198.168.1.5  
**Subnet Mask:** 255.255.255.0

Now, in binary:

```
IP:   11000000.10101000.00000001.00000101  
Mask: 11111111.11111111.11111111.00000000
```

---

### ⚙️ What the 255 Means

- Each **255** = all 8 bits are **locked** (`11111111`)  
    → That means **this part of the address cannot change** — it’s the **network portion**.
    
- Each **0** = all 8 bits are **unlocked** (`00000000`)  
    → That means **this part can vary** — it’s the **host portion**.
    

---

### 🧩 In Plain Terms

- Every device in the same subnet will share the **same network bits** (the 255 parts).
    
- Only the **host bits** (the 0 parts) will differ — that’s what gives each device its own unique IP within that subnet.
    
- So in `198.168.1.0/24`, all devices must start with `198.168.1`, but the last number (0–255) changes per host.
    

---

### 💡 Quick Analogy

Think of it like an **apartment building**:

- `198.168.1` = the **building address** (network part)
    
- `.5` = the **apartment number** (host part)
    
- The subnet mask says **which digits are the building address** (255 = fixed) and **which are apartment numbers** (0 = variable).
    

---

### 🧾 TL;DR Summary

|Part|Binary|Meaning|
|---|---|---|
|255|`11111111`|Locked (network)|
|0|`00000000`|Unlocked (host)|
|Subnet mask|Defines which bits are fixed (network) and which can vary (host)||
|Purpose|Keeps devices grouped logically, reduces chaos, and helps routing||

---

Would you like me to make this formatted like a printable 1-page flashcard or cheat sheet (bold headers, boxes, colors, etc.)?