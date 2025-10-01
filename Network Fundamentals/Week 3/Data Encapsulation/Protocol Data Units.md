As data moves down the TCP/IP stack to be sent, each layer adds its own information to the data — this process is called **encapsulation**. At each layer, the data takes on a new name called a **Protocol Data Unit (PDU)**, which reflects the role it plays at that layer.

- **Application Layer → Data** (user information ready to send)
    
- **Transport Layer → Segment (TCP) / Datagram (UDP)** (adds port numbers, sequencing, reliability info)
    
- **Network Layer → Packet (or IP Datagram)** (adds source and destination IP addresses for routing)
    
- **Data Link Layer → Frame** (adds MAC addresses and error checking for delivery on the local network)
    
- **Physical Layer → Bits** (converts into 1s and 0s on the wire, fiber, or air for transmission)
    

At the receiving side, the process reverses: each layer removes its header and passes the remaining data up until it reaches the application again.![[Screenshot 2025-08-29 at 22-35-47 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]