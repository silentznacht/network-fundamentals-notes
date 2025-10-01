In an Ethernet LAN, every device is connected to the same shared media, and communication between devices relies on **MAC (Media Access Control) addresses** to identify the physical source and destination NICs on the local network. A MAC address operates at the **data link layer** of the OSI model and is a **48-bit (6-byte) identifier**, usually written as 12 hexadecimal digits. To ensure uniqueness, vendors are assigned a **24-bit Organizationally Unique Identifier (OUI)** by the IEEE, which forms the first half of the MAC address, while the remaining 24 bits are a unique vendor-assigned value. For example, Cisco’s OUI `00-60-2F` combined with a unique value `3A-07-BC` forms the MAC address `00-60-2F-3A-07-BC`. Although MAC addresses are intended to be unique, duplicates can occur due to manufacturing errors, virtual machine configurations, or software modifications, in which case the MAC may need to be changed or reassigned.

**Located**

Sometimes the MAC address is referred to as a burned-in address (BIA) because the address is hard coded into read-only memory (ROM) on the NIC. This means that the address is encoded into the ROM chip permanently.

**When the computer boots up, the NIC copies its MAC address from ROM into RAM. When a device is forwarding a message to an Ethernet network, the Ethernet header includes these:**

- **Source MAC address** - This is the MAC address of the source device NIC.
- **Destination MAC address** - This is the MAC address of the destination device NIC.

**NIC** 

When a NIC receives an Ethernet frame, it examines the destination MAC address to see if it matches the physical MAC address that is stored in RAM. If there is no match, the device discards the frame. If there is a match, it passes the frame up the OSI layers, where the de-encapsulation process takes place.

**Note:** Ethernet NICs will also accept frames if the destination MAC address is a broadcast or a multicast group of which the host is a member.

Any device that is the source or destination of an Ethernet frame, will have an Ethernet NIC and therefore, a MAC address. This includes workstations, servers, printers, mobile devices, and routers.