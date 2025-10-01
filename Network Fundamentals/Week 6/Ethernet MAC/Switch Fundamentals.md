Now that you know all about Ethernet MAC addresses, it is time to talk about how a switch uses these addresses to forward (or discard) frames to other devices on a network. If a switch just forwarded every frame it received out all ports, your network would be so congested that it would probably come to a complete halt.

A Layer 2 Ethernet switch uses Layer 2 MAC addresses to make forwarding decisions. It is completely unaware of the data (protocol) being carried in the data portion of the frame, such as an IPv4 packet, an ARP message, or an IPv6 ND packet. The switch makes its forwarding decisions based solely on the Layer 2 Ethernet MAC addresses.

An Ethernet switch examines its MAC address table to make a forwarding decision for each frame, unlike legacy Ethernet hubs that repeat bits out all ports except the incoming port. In the figure, the four-port switch was just powered on. The table shows the MAC Address Table which has not yet learned the MAC addresses for the four attached PCs.

SImplified 

MAC Address table:

A **MAC address table** is a switch’s little “address book” that keeps track of which devices (MAC addresses) are connected to which ports. When a frame arrives, the switch looks at the destination MAC and checks the table to send the frame only to the correct port. If the MAC isn’t in the table yet, the switch sends the frame to all other ports and adds the source MAC to the table for next time. Each entry has a timer so the switch forgets devices that disappear. This helps the switch deliver frames efficiently and avoid unnecessary traffic.

**Learn**:
When a frame comes into a switch, the switch looks at the **destination MAC address** to figure out which port to send it out. If it already knows the port for that MAC, it sends the frame only there. If it doesn’t know, it sends the frame to all other ports except the one it came from. At the same time, the switch **learns the source MAC and the port it came in on** and stores it in its **MAC address table**, which is like a little address book that remembers which devices are on which ports. This helps the switch send data efficiently and avoid flooding the network.

**Forward:**

When a switch receives a frame, it first looks at the **destination MAC address**. If it’s a **unicast address** (for a single device), the switch checks its MAC address table. If the MAC is in the table, the switch sends the frame only to the correct port. If it isn’t in the table, the switch floods the frame to all ports except the one it came from; this is called an **unknown unicast**. If the destination MAC is a **broadcast** or **multicast** address, the switch also floods the frame to all ports except the incoming one.