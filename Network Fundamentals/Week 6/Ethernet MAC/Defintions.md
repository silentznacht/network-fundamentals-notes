
**Different Cast Types (Unicast, Broadcast, Multicast):**

- **Unicast:** One-to-one (NIC checks MAC, only match accepts).
- **Broadcast:** One-to-all (`FF:FF:FF:FF:FF:FF`, ARP/DHCP).
- **Multicast:** One-to-many selective (`01:00:5E`, IGMP/MLD groups).

In Ethernet networks, frames can be delivered in three ways: unicast, broadcast, and multicast. **Unicast** communication is one-to-one, where the frame’s destination MAC address is compared by each NIC at the MAC sublayer; only the device whose MAC matches accepts the frame, while others discard it. **Broadcast** communication is one-to-all, using the special destination MAC address `FF:FF:FF:FF:FF:FF`, which every device on the local network processes—this is how protocols like ARP and DHCP discover work. **Multicast** communication is one-to-many but selective, using reserved multicast MAC addresses (e.g., `01:00:5E` for IPv4). Devices subscribe to specific multicast groups through higher-layer protocols such as IGMP (IPv4) or MLD (IPv6), and only members of those groups accept and process the frames. Together, these three methods define how Ethernet delivers data across a LAN depending on whether it’s intended for a single device, all devices, or a selected group.

**Simplified:** 

**Broad:** 
All devices on the network receive this frame (all communication)

An Ethernet broadcast frame is received and processed by every device on the Ethernet LAN. **The features of an Ethernet broadcast are as follows:**

- It has a destination MAC address of FF-FF-FF-FF-FF-FF in hexadecimal (48 ones in binary).
- It is flooded out all Ethernet switch ports except the incoming port.
- It is not forwarded by a router.

**Unicast:**
A unicast MAC address is the unique address that is used when a frame is sent from a single transmitting device to a single destination device.

**Multicast:**
An Ethernet multicast frame is received and processed by a group of devices on the Ethernet LAN that belong to the same multicast group**. The features of an Ethernet multicast are as follows:
	- There is a destination MAC address of 01-00-5E when the encapsulated data is an IPv4 multicast packet and a destination MAC address of 33-33 when the encapsulated data is an IPv6 multicast packet.
	- There are other reserved multicast destination MAC addresses for when the encapsulated data is not IP, such as Spanning Tree Protocol (STP) and Link Layer Discovery Protocol (LLDP).
	- It is flooded out all Ethernet switch ports except the incoming port, unless the switch is configured for multicast snooping.
	- It is not forwarded by a router, unless the router is configured to route multicast packets.

In Ethernet, a multicast frame is delivered only to devices that have joined a specific multicast group. IPv4 multicast frames use destination MAC addresses starting with `01:00:5E`, while IPv6 uses `33:33`; other protocols like STP and LLDP have their own special multicast MACs. Switches typically send multicast frames out all ports except the one it came from, unless configured for multicast snooping, and routers normally do not forward multicast unless specifically set to do so. Multicast IP addresses are group addresses — `224.0.0.0` to `239.255.255.255` for IPv4 and `ff00::/8` for IPv6 — with the source always being a unicast address. Each multicast IP maps to a corresponding multicast MAC, and only NICs subscribed to that MAC accept and process the frame, while all others ignore it. Multicast allows one device to efficiently send data to a selected group rather than to every device on the network.