# IPv6 Addressing & Discovery — Plain English Version

---

## 1️⃣ **RS & RA Messages**

- **RS = Router Solicitation** → “Hey router, I just showed up. What network should I use?”
    
- **RA = Router Advertisement** → Router replies: “Here’s the network prefix, subnet info, and how to make your IPv6 address.”
    

**Bottom line:** Your computer asks → router answers → your device knows how to talk to the network.

---

## 2️⃣ **How Your Device Gets an IPv6 Address**

There are a few ways:

### **A. SLAAC (Self-Assigning)**

- Device uses **the info from the router** (RA message) and makes its **own address**.
    
- Works without a server.
    
- Needs a way to make an **interface ID** (like a “device ID”) to complete the address.
    

### **B. Stateless DHCPv6**

- Device **makes its own IP** like SLAAC, but asks a DHCP server for **extras** (DNS server, etc.).
    
- Server doesn’t pick the IP — it just hands out extra info.
    

### **C. Stateful DHCPv6**

- DHCP server **assigns the entire IP** and other info.
    
- Works like classic IPv4 DHCP.
    

---

## 3️⃣ **Interface IDs (the device part of the address)**

Your IPv6 address has two parts:

```
[Network prefix / Subnet ID] : [Interface ID]
```

The **Interface ID** is the device-specific part. There are two ways to get it:

### **1. EUI-64 (from MAC address)**

- Converts your network card’s MAC into the last 64 bits of the IPv6 address.
    
- Stable and unique — but anyone could figure out your device from it.
    

### **2. Randomly generated**

- Device makes a **random number** for the interface ID.
    
- Temporary and privacy-friendly — good for internet traffic so your MAC isn’t exposed.
    

---

## 4️⃣ **How It All Fits Together**

1. Device turns on → sends **RS**
    
2. Router replies with **RA**
    
3. Device sees:
    
    - Should I **self-assign**? (SLAAC)
        
    - Do I need **extra info**? (Stateless DHCPv6)
        
    - Or should I **wait for the server to assign**? (Stateful DHCPv6)
        
4. Device picks **interface ID** (EUI-64 or random)
    
5. Device now has a working IPv6 address and knows the gateway
    

---

### TL;DR — The “What It Means” Version

- **RS/RA:** Device asks, router answers
    
- **SLAAC:** Device makes its own IP from the network info
    
- **Stateless DHCPv6:** Device makes its own IP, server gives extras
    
- **Stateful DHCPv6:** Server gives you the full IP
    
- **EUI-64:** Uses MAC for device ID → stable but exposes your hardware
    
- **Random:** Device ID is random → protects privacy
    
- **Link-Local (`fe80::`)** → Only works on your network segment
    
- **Global Unicast (`2001:…`)** → Works on the internet
    