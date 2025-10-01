**Address Resolution Protocol (ARP)->** ARP is a network protocol used to map an IP address to a physical MAC address within a local network.
	- When a device wants to communicate with another address on the same network, it needs to know the recipents MAC address. ARP helps by sending out a broadcast request asking "Who has this IP address?". The device with the matching IP address responds with its MAC address

**Essentially:** ARP is a broadcast. It sends out a request for a distinct IP address, then the device with the same IP address responds.

**ARP = broadcast request for “Who owns this IP?” → the owner responds with their MAC.**

### **MAC Address (Media Access Control Address)**

- Think of it as the **serial number** for your network card.
    
- Every network device (laptop, router, phone) has a **unique MAC address** burned into its hardware.
    
- Looks like this: `00:1A:2B:3C:4D:5E`.
    
- Used only **within the local network (LAN)** — not across the internet.

ARP essentially resolves an IP address to the device’s MAC address, so a client knows where to send data on the local network.