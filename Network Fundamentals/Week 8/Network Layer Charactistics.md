
- The Network Layer (OSI Layer 3) allows end devices to exchange data across networks
	- **IP version 4 (IPv4)** and **IP version 6 (IPv6)** are the principal network layer communication protocols.
	- Other network layer protocols includnig routing protocols, such as **Open Shortest Path First (OSPF)** and messaging protocols such **Internet Control Message Protocol (ICMP)**.
- TO accomplish end to end communications across network boundaries, network layer protocols perform four basic operations
	- **Addressing end devices** 
		- End devices must be configured with a unique IP address for identification on the network. (Each device has a unique IP address)
	- **Encapsulation**
		- The network layer encapsulates the protocol data unit (PDU) from the transport layer into a packet. The encapsulation process then adds IP header information, such as the IP address of the source (sending) and destination (recieving) hosts. The encapsulation process os performed by the source of the IP packet (sender).
	- **Routing**
		- The network layer provides services to direct the packets to a destination host on another network. To travel to other netowkrs, the packet must be processed by the router. The role of the router is to select the best path and direct packets toward the destination host in a process known as routing. A packet may cross many routers before reaching the destination host. Each router a packet crosses to reach the destination host is called a hop.
	- **De-encapsulation**
		- When the packer arrives at the network layer of the destination host, the host checks the IP header of the packet. 
			- If the destination IP address within the header matches it's own IP address, the IP header is removed from the packer. After the packet is de-encapsulated by the network layer, the resulting Layer 4 PDU is passed up to the appropriate service at the transport layer. The de-encapsulation process is performed by the destination host of the IP packet.
-  Unlike the transport layer (OSI Layer 4), which manages the data transport between the processes running on each host, network layer communication protocols (i.e., IPv4 and IPv6) specify the packet structure and processing used to carry the data from one host to another host. Operating without regard to the data carried in each packet allows the network layer to carry packets for multiple types of communications between multiple hosts.

**IP Encapsulation** - IP encapsulates the transport layer (the layer just above the network layer) segment or other data by adding an IP header. The IP header is used to deliver the packet to the destination host.![[Screenshot 2025-09-30 at 18-59-17 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

The IP header is examined by Layer 3 devices (i.e., routers and Layer 3 switches) as it travels across a network to its destination. It is important to note, that the IP addressing information remains the same from the time the packet leaves the source host until it arrives at the destination host, except when translated by the device performing Network Address Translation (NAT) for IPv4.

**Routers** - Routers implement routing protocols to route packets between networks. THie routing performed by these intermediary devices examines the network layer addressing in the packet header.