**Host** is basically any **device that can send or receive data on a network**. Think of it as the “end point” in a network conversation.

- IPv4 and IPv6, packets are always created at the source host. The source host must be able to direct the packet to the destination host. To do this, host end devices create their own routing table

- Another role of the network layer is to direct packets between hosts. A host can send a packet to the following: (Direct packets between devices ie hosts)
	- **Itself** (a device pinging itself) - A host can ping itself by sending a packet to a special IPv4 address of 127.0.0.1 or an IPv6 address ::1, which is referred to as the loopback interface. Pinging the loopback interface tests the TCP/IP protocol stack on the host. 
	- **Local host** (a src device pinging its dst device)- This is a destination host that is on the same local network as the sending host. The source and destination hosts share the same network address.
	- **Remote host** (a host can send a packet to another network) - This is a destination host on a remote network. The source and destination hosts do not share the same network address.
- **Whether a packet is destined for a local host or a remote host is determined by the source end device.** **The source end device determines whether the destination IP address is on the same network that the source device itself is on.** The method of determination varies by IP version:
	- **In IPv4** - The source device uses its own subnet mask along with its own IPv4 address and the destination IPv4 address to make this determination.
	- **In IPv6** - The local router advertises the local network address (prefix) to all devices on the network.
		- Essentially IPv4 and IPv6 determines whether the destination host is in network or outside of the network.
			- If outside of the network, it then sends the packet to the default gateway / router
			- If in network, it forwards the packet to the layer 2 switch, the layer 2 switch checks the packet for the senders MAC address, then checks its MAC address table and forwards it to the right port.
- **Default Gateway**
	- The default gateway is the network device (i.e., router or Layer 3 switch) that can route traffic to other networks.
	
	- On a network, a default gateway is usually a router with these features:
		- It has a local IP address in the same address range as other hosts on the local network.
		- It can accept data into the local network and forward data out of the local network.
		- It routes traffic to other networks.