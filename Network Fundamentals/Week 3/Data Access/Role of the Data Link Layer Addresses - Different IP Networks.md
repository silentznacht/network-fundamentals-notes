When two devices are on **different networks**, a computer can’t just send its Ethernet frame straight to the destination device (because it’s not on the same local network). Instead, it sends the frame to its **default gateway (router)**. The router has a MAC address that lives on the same local network as the computer, so the computer can reach it. In this case, the **source MAC** is the PC’s MAC, and the **destination MAC** is the router’s MAC. The router then takes care of forwarding the packet toward the real destination on the other network.

**Simplified:**

**Essentially:** When a device wants to communicate with a server that is outside its local network, it first needs to reach its **router (default gateway)**. The device uses **ARP** to broadcast a request asking, _“Who has this IP?”_ The router responds with its **MAC address**, allowing the device to send Ethernet frames to it. Once the router receives the frames, it forwards the message toward the destination server, effectively bridging communication between the local device and the remote server.

**HOST TO ROUTER**

![[Screenshot 2025-08-29 at 22-55-51 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

**ROUTER TO ROUTER**
![[Screenshot 2025-08-29 at 22-57-50 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

**ROUTER TO SERVER**
![[Screenshot 2025-08-29 at 23-06-33 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]