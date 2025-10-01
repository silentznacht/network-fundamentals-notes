
**Trailer (error detection)**

Data link layer protocols add a trailer to the end of each frame. In a process called error detection, the trailer determines if the frame arrived without error. It places a logical or mathematical summary of the bits that comprise the frame in the trailer. The data link layer adds error detection because the signals on the media could be subject to interference, distortion, or loss that would substantially change the bit values that those signals represent.

**Other**
The **Frame Check Sequence (FCS)** in the Ethernet trailer is used for error detection. When sending a frame, the transmitter calculates a value called the **Cyclic Redundancy Check (CRC)**, which summarizes the contents of the frame, and places it in the FCS field. When the frame is received, the receiver recalculates the CRC and compares it to the FCS value. If they match, the frame is valid; if not, the frame is assumed corrupted and discarded.

### Key points:

- A **MAC address** is a hardware “name tag” burned into the network interface card (NIC). It’s **globally unique**, but it says nothing about _where_ the device is.
    
- An **IP address** is hierarchical and tied to the device’s _location in a network_ (like a mailing address that changes when you move).

Every device has a unique **MAC address** that stays the same no matter what network it connects to. The Data Link layer uses this MAC to identify and communicate with devices **within the same local network**. However, MAC addresses are not hierarchical and do not indicate network location — to communicate across different networks, devices rely on **IP addresses and Layer 3 routing**.


**IMPORTANT**

**Layer 2 (Data Link)** uses MAC addresses for **local delivery** within the same network. When data needs to travel to a **different network**, a **router** checks the **IP address (Layer 3)** to determine the destination network and forwards the data accordingly, giving it new Layer 2 information for the next segment. In short, **Layer 2 handles local delivery**, while **Layer 3 enables communication across networks**.

The data link layer address is only used for local delivery. Addresses at this layer have no meaning beyond the local network. Compare this to Layer 3, where addresses in the packet header are carried from the source host to the destination host, regardless of the number of network hops along the route.

If the data must pass onto another network segment, an intermediary device, such as a router, is necessary. The router must accept the frame based on the physical address and de-encapsulate the frame in order to examine the hierarchical address, which is the IP address. Using the IP address, the router can determine the network location of the destination device and the best path to reach it. When it knows where to forward the packet, the router then creates a new frame for the packet, and the new frame is sent on to the next network segment toward its final destination.