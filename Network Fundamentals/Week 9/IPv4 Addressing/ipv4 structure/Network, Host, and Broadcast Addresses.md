Simplified: 
- Network Address - A unique address that repersents a specific network, which often used to identify a host in a subnet.
	- Subnet hosts are often routers, since a router is the access point to a network
	- Subnetting / subnets work are mandatory for an efficent network, it is for optimization to avoid latency and congestion due to too many devices communicating at once. This means a main router, being connected to several other router, each other router than the main router, repersents a host / access point to a subnet.
	
- Host Addresses- an address tha tis assigned to a host within a network, ie routers, laptops, phones, printers etc. A host is identified by the host portion of its address ie 192.168.4.15 with a subnet mask of 255.255.255.0, means that 192.168.4 is the network portion of the address used to identify the network the host is in, and .15 identifies the host itself within that network.
 
- Broadcast Addresses - To explain, every network address comes with a prefixed length ie 192.168.5.0/24 255.255.255.0 (ie 24 bits locked). The /24 at the end repsersents the amounts of bits / octets locked for the network portion of the address, but also displays a range for the host portion, since 192.168.5 are locked bits, then that means the host portion .0 has a specific range from 0 - 255, meaning hosts and nodes on a network can have a host portion to their IP within 0 - 255. What is important is that a broadcast address, is the very last address on the host portion of an address meaning 255, this means you are broadcasting all hosts within that range. An example is if you have 2 hosts ie PCs, PC 1 = 192.12.100.6 255.255.255.0  and PC 2 192.12.100.10, then sending a broadcast frame to address 192.12.100.255 means you are sending a message to all of the hosts on that network.

Every network address comes with a **prefix length** (for example, `192.168.5.0/24`) that determines how many bits are reserved for the **network portion** versus how many are available for the **host portion**.

- The `/24` means **24 bits** are “locked” for the network part — in other words, the first three octets (`192.168.5`) identify the **network**, and the **last octet** is reserved for **hosts**.
    
- Because an octet is 8 bits, the host portion can range from **0 to 255** (a total of 256 possible addresses).
    

	However, two of these addresses are **special and cannot be assigned** to hosts:
	1. The **network address** (`192.168.5.0`), which identifies the network itself.
	    
	2. The **broadcast address** (`192.168.5.255`), which is the _last address in the subnet_ and is used to send messages to **all hosts** within that network.
	    
	
	For example:
	- PC1 → `192.12.100.6` (Subnet Mask: `255.255.255.0`)
	    
	- PC2 → `192.12.100.10` (Subnet Mask: `255.255.255.0`)
	    
	
	If a packet is sent to the **broadcast address** `192.12.100.255`, both PC1 and PC2 (and every other host in the same subnet) will receive it.
	
	Within each network are three types of IP addresses:
	
	- Network address
	- Host addresses
	- Broadcast address

**Network address**

**A network address is an address that represents a specific network. A device belongs to this network if it meets three criteria:**

- It has the same subnet mask as the network address.
- It has the same network bits as the network address, as indicated by the subnet mask.
- It is located on the same broadcast domain as other hosts with the same network address.

A host determines its network address by performing an AND operation between its IPv4 address and its subnet mask.

**Host addresses**

Host addresses are addresses that can be assigned to a device such as a host computer, laptop, smart phone, web camera, printer, router, etc. The host portion of the address is the bits indicated by 0 bits in the subnet mask. Host addresses can have any combination of bits in the host portion except for all 0 bits (this would be a network address) or all 1 bits (this would be a broadcast address).

**Broadcast address**

A broadcast address is an address that is used when it is required to reach all devices on the IPv4 network. As shown in the table, the network broadcast address has all 1 bits in the host portion, as determined by the subnet mask.