IEEE 802 LAN/MAN protocols, including Ethernet, use the following two separate sublayers of the data link layer to operate. They are the Logical Link Control (LLC) and the Media Access Control (MAC), as shown in the figure.

Recall that LLC and MAC have the following roles in the data link layer:

- **LLC Sublayer** - This IEEE 802.2 sublayer communicates between the networking software at the upper layers and the device hardware at the lower layers. It places information in the frame that identifies which network layer protocol is being used for the frame. This information allows multiple Layer 3 protocols, such as IPv4 and IPv6, to use the same network interface and media.
- **MAC Sublayer** - This sublayer (IEEE 802.3, 802.11, or 802.15 for example) is implemented in hardware and is responsible for data encapsulation and media access control. It provides data link layer addressing and is integrated with various physical layer technologies.

**The MAC sublayer is responsible for data encapsulation and accessing the media.**

**Simplified Summary:** 

When a user sends data, **Layer 3 (IPv4/IPv6)** creates a packet with source and destination IP addresses. **Layer 2 (Data Link Layer)** then encapsulates it: the **LLC sublayer** adds a protocol identifier so the receiver knows which Layer 3 protocol should handle the payload, and the **MAC sublayer** adds a header and trailer (MAC addresses and error-checking info) to create a frame. The **physical layer** converts the frame into signals sent over the network. If the frame passes through a **switch**, the switch reads the destination MAC and forwards it to the correct port. At the destination, MAC checks addresses and errors, LLC reads the protocol label, and Layer 3 processes or routes the packet. This layered process allows multiple protocols to share the same network interface efficiently and ensures accurate delivery.
**LLC (Logical Link Control)**

- Labels the packet with the **Layer 3 protocol** used (e.g., IPv4, IPv6, ARP), so the receiving device knows which protocol should handle the payload.
    

**MAC (Media Access Control)**

- Takes the packet and encapsulates it into a **Layer 2 frame** by adding a **header** (source and destination MAC addresses) and a **trailer** (error detection/FCS) to ensure correct delivery over the network.
- 
- ![[Screenshot 2025-09-17 at 19-59-38 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]