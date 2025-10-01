
The IP packet contains two IP addresses:

- **Source IP address** - The IP address of the sending device, which is the original source of the packet.
- **Destination IP address** - The IP address of the receiving device, which is the final destination of the packet.

The IP addresses indicate the original source IP address and final destination IP address. This is true whether the source and destination are on the same IP network or different IP networks.

An IP address contains two parts:

- **Network portion (IPv4) or Prefix (IPv6)** - The left-most part of the address that indicates the network in which the IP address is a member. All devices on the same network will have the same network portion of the address.
- **Host portion (IPv4) or Interface ID (IPv6)** - The remaining part of the address that identifies a specific device on the network. This portion is unique for each device or interface on the network.

**Note:** The subnet mask (IPv4) or prefix-length (IPv6) is used to identify the network portion of an IP address from the host portion.![[Screenshot 2025-08-29 at 22-43-56 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]