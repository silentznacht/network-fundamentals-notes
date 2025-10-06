***ARP is exclusive to only LAN based networks***

- Every IP device on an Ethernet network has a unique Ethernet MAC address. When a device sends an Ethernet Layer 2 frame, it contains these two addresses:

	- **Destination MAC address** - The Ethernet MAC address of the destination device on the same local network segment. If the destination host is on another network, then the destination address in the frame would be that of the default gateway (i.e., router).
	- **Source MAC address** - The MAC address of the Ethernet NIC on the source host.
- To send a packet to another host on the same local IPv4 network, a host must know the IPv4 address and the MAC address of the destination device. Device destination IPv4 addresses are either known or resolved by device name. However, MAC addresses must be discovered.

- A device uses Address Resolution Protocol (ARP) to determine the destination MAC address of a local device when it knows its IPv4 address.

	- ARP provides two basic functions:
		- Resolving IPv4 addresses to MAC addresses
		- Maintaining a table of IPv4 to MAC address mappings