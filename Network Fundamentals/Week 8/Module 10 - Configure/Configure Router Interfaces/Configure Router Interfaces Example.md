![[Screenshot 2025-10-05 at 17-14-50 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]
# 🧠 Cisco Router Interface Configuration – Study Notes

## 🔹 1. Enter Privileged EXEC Mode

```bash
R1> enable
```

- Grants access to **privileged EXEC mode** (`R1#`) where advanced commands are available.
    
- Without this, you can only view basic info.
    

---

## 🔹 2. Enter Global Configuration Mode

```bash
R1# configure terminal
```

- Switches into **global configuration mode** (`R1(config)#`) to make permanent changes to the router.
    
- Used for configuring interfaces, routing, passwords, etc.
    

---

## 🔹 3. Configure Interface GigabitEthernet 0/0/0 (LAN)

```bash
R1(config)# interface gigabitEthernet 0/0/0
R1(config-if)# description Link to LAN
R1(config-if)# ip address 192.168.10.1 255.255.255.0
R1(config-if)# ipv6 address 2001:db8:acad:10::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
```

**Explanation:**

- `interface gigabitEthernet 0/0/0` → Selects the physical port to configure.
    
- `description Link to LAN` → Adds a label for clarity/documentation.
    
- `ip address 192.168.10.1 255.255.255.0` → Assigns IPv4 address and subnet mask.
    
- `ipv6 address 2001:db8:acad:10::1/64` → Assigns IPv6 address.
    
- `no shutdown` → Enables the interface (interfaces are off by default).
    
- `exit` → Returns to global config mode.
    

**System Messages:**

```
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0/0, changed state to up
```

➡️ The port is now active and passing traffic.

---

## 🔹 4. Configure Interface GigabitEthernet 0/0/1 (WAN / Router-to-Router)

```bash
R1(config)# interface gigabitEthernet 0/0/1
R1(config-if)# description Link to R2
R1(config-if)# ip address 209.165.200.225 255.255.255.252
R1(config-if)# ipv6 address 2001:db8:feed:224::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
```

**Explanation:**

- `interface gigabitEthernet 0/0/1` → Selects second port (usually WAN or another router).
    
- `description Link to R2` → Notes this connects to Router 2.
    
- `ip address 209.165.200.225 255.255.255.252` → Assigns IPv4 address (point-to-point subnet).
    
- `ipv6 address 2001:db8:feed:224::1/64` → Assigns IPv6 address.
    
- `no shutdown` → Enables the port.
    
- `exit` → Returns to global config mode.
    

**System Messages:**

```
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/1, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface GigabitEthernet0/0/1, changed state to up
```

➡️ Interface successfully activated and connected to R2.

---

## 🔹 5. Verify Interfaces

```bash
R1# show ip interface brief
```

**Purpose:**  
Displays all interfaces, their assigned IPs, and current operational status.

**Example Output:**

```
Interface              IP-Address      OK? Method Status  Protocol
GigabitEthernet0/0/0   192.168.10.1    YES manual up      up
GigabitEthernet0/0/1   209.165.200.225 YES manual up      up
```

**Key Columns:**

- **Interface:** The physical or logical port name.
    
- **IP-Address:** Assigned IPv4 address.
    
- **Status:** “Up” = administratively enabled.
    
- **Protocol:** “Up” = link is active and passing data.
    

---

## 🧩 Concept Summary

| Concept                     | Description                                                                |
| --------------------------- | -------------------------------------------------------------------------- |
| **Interface**               | Physical or virtual connection point on a router.                          |
| **GigabitEthernet 0/0/0**   | Port connected to the LAN.                                                 |
| **GigabitEthernet 0/0/1**   | Port connected to another router (WAN).                                    |
| **IP Address**              | Identifies the router on a network. Each interface must have a unique one. |
| **Description**             | Notes the purpose of each interface (helps documentation).                 |
| **no shutdown**             | Activates the interface (otherwise it stays “administratively down”).      |
| **show ip interface brief** | Verifies interface configuration and operational status.                   |

---

### 🧠 Quick Recap

- Use `enable` → `configure terminal` to start setup.
    
- Configure interfaces with `ip address`, `ipv6 address`, and `no shutdown`.
    
- Always verify with `show ip interface brief`.
    
- Each interface = separate network connection (LAN/WAN).
    