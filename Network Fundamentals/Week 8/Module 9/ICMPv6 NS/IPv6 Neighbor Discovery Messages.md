
- IPv6 Neighbor Discovery protocol is sometimes referred to as ND or NDP. ND provides address resolution, router discovery, and redirection services for IPv6 using ICMPv6. ICMPv6 ND uses five ICMPv6 messages to perform these services:
	- Neighbor Solicitation messages
		- Neighbor Solicitation and Neighbor Advertisement messages are used for device-to-device messaging such as address resolution (similar to ARP for IPv4). Devices include both host computers and routers.
	- Neighbor Advertisement messages
		- Router Solicitation and Router Advertisement messages are for messaging between devices and routers. Typically router discovery is used for dynamic address allocation and stateless address autoconfiguration (SLAAC).
	- Router Solicitation messages
	- Router Advertisement messages
	- Redirect Message