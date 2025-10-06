- An ARP request is sent when a device needs to determine the MAC address that is associated with an IPv4 address, and it does not have an entry for the IPv4 address in its ARP table.
	- **To simplify**, an ARP request is sent when a host has the destination devices IPv4 address but not it's MAC Address.

- ARP messages are encapsulated directly within an Ethernet frame. There is no IPv4 header. The ARP request is encapsulated in an Ethernet frame using the following header information:

- **Destination MAC address** - This is a broadcast address FF-FF-FF-FF-FF-FF requiring all Ethernet NICs on the LAN to accept and process the ARP request.
- **Source MAC address** - This is MAC address of the sender of the ARP request.
- **Type** - ARP messages have a type field of 0x806. This informs the receiving NIC that the data portion of the frame needs to be passed to the ARP process.

	- Because ARP requests are broadcasts, they are flooded out all ports by the switch, except the receiving port. All Ethernet NICs on the LAN process broadcasts and must deliver the ARP request to its operating system for processing. Every device must process the ARP request to see if the target IPv4 address matches its own. A router will not forward broadcasts out other interfaces.
	
- **Simplified:** In short, an ARP request is encapsulated inside an Ethernet frame and sent to the switch. The switch **floods the frame out all ports** (except the incoming port), so all devices on the LAN receive it. Each device then checks if the requested IP matches its own and responds if it does.