
## 📘 IPv6 Address Notation Rules (Simplified Study Notes)

### 🧩 Basics

- **IPv6 addresses** are **128 bits long**.
    
- Written as **8 groups** (called **hextets**) of **4 hexadecimal digits**, separated by colons (`:`).  
    Example: `2001:0db8:0000:0000:00a0:0c2f:0000:0001`
    
- Each hextet = **16 bits** (2 bytes).
    
- IPv6 is **not case-sensitive** (uppercase or lowercase both valid).
    

---

### 🔹 Rule 1: Omit Leading Zeros

- You can remove **leading zeros** in each hextet (zeros at the _start_).
    
- You **cannot** remove **trailing zeros**, since that changes the value.
    

**Examples:**

|Original|Shortened|
|---|---|
|`01ab`|`1ab`|
|`00ab`|`ab`|
|`0a00`|`a00`|
|`09f0`|`9f0`|

**Example address:**  
`2001:0db8:0000:0000:00a0:0c2f:0000:0001` → `2001:db8:0:0:a0:c2f:0:1`

---

### 🔹 Rule 2: Use Double Colon (::) for Consecutive Zero Hextets

- A **double colon (`::`)** can replace **a single continuous sequence** of one or more all-zero hextets.
    
- This is called **compressed format**.
    

**Example:**  
`2001:db8:cafe:1:0:0:0:1` → `2001:db8:cafe:1::1`

**⚠️ Important:**

- You can use **`::` only once** per address.  
    ❌ `2001:db8::abcd::1234` is invalid — too many double colons.
    
- If there’s more than one zero sequence, compress **the longest** one.  
    If equal length, compress **the first**.
    

---

### ✅ Combined Example

Start: `2001:0db8:0000:0000:00a0:0c2f:0000:0001`  
→ Remove leading zeros: `2001:db8:0:0:a0:c2f:0:1`  
→ Compress zeros: `2001:db8::a0:c2f:0:1`

---

### 🧠 Quick Summary Table

|Rule|Description|Example|
|---|---|---|
|**1**|Remove leading zeros in any hextet|`0db8 → db8`|
|**2**|Replace one or more all-zero hextets with `::`|`2001:db8:0:0:0:0:0:1 → 2001:db8::1`|
|**Limit**|Only one `::` allowed per address|❌ `2001:db8::1::1`|

---

Would you like me to format this for easy printing (like a one-page PDF study sheet)?
  