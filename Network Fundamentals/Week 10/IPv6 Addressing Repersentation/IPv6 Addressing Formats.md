
**Note:** IPv6 addresses are much larger than IPv4 addresses, which is why we are unlikely to run out of them.

**Note:** IPv6 addresses are 128 bits in length and written as a string of hexadecimal values. Every four bits is represented by a single hexadecimal digit; for a total of 32 hexadecimal values, as shown in the figure. IPv6 addresses are not case-sensitive and can be written in either lowercase or uppercase.
![[Pasted image 20251102165034.png]]
**4 hexadecimal digits = 16 binary digits**

In IPv6, each **group of 16 bits** (2 bytes) is an "octet" (or "hextet"), and this group is represented by **four hexadecimal digits**.

When writing an **IPv6 address**, you’re allowed to **shorten it** by removing any **leading zeros** (the zeros that appear at the _start_ of a four-digit section), but **not** the ones at the _end_.

IPv6 addresses are written in **eight groups of four hexadecimal digits** (called _hextets_), separated by colons — for example:  
`2001:0db8:0000:0000:00a0:0c2f:0000:0001`

Since that’s a lot to type, there are rules to shorten it.  
This rule says:

- You can remove zeros **at the start of a hextet**.  
    ✅ `01ab` → `1ab`  
    ✅ `00ab` → `ab`
    
- But **don’t remove zeros at the end**, because it could change the meaning.  
    ❌ `abc0` ≠ `abc`
    

For example,  
`2001:0db8:0000:0000:00a0:0c2f:0000:0001`  
can be simplified to  
`2001:db8:0:0:a0:c2f:0:1`

You’re just making it shorter **without changing what the address means**.