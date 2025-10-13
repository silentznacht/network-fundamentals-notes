
Three commonly used numeric addresses on a network.

**Port address (identifies an application)**
- Each client or server application running on a computer is identified by a port address, also called a port or a port number.
- For example, a web server receives communication from a browser at port 80 using the HTTP protocol for unsecured communication and at port 443 using the HTTPS protocol for secured communication.
- In short, every server application running on a computer is identified by a port address.

**IP address (identifies a node and its network connection)**
- An IP address is assigned to a node when the device first connects to the network, and it identifies the network connection.
- The following are two types of IP addresses:
	- IPv4 (binary string) - A 32-bit string, written as four decimal numbers called octets and separated by periods, such as 192.168.100.4
	- IPv6 (hexadecimal string) - A 128-bit string, written as eight hexadecimal numbers separated by colons, such as 2001:0000:B80:0000:0000:D3:9C5A:CC

**MAC address (identifies a network adapter)**
- Every wired or wireless network adapter, also called a **network interface card (NIC),** has a 48-bit (6-byte) identification number—called the **MAC address, physical address, or network adapter address.
	- **Simplified:** Every device has a NIC, the NIC has a unique MAC address that is used so that other devices on the same network, can communicate with each other.
		- Example, just like in your network fundamentals class, its like how a device can send out an ARP request for the routers NIC through an IP address (i.e whoever has this ip please give me your mac address)
 - All MAC addresses are hard coded onto the NIC by its manufacturer.
 - Part of the MAC address identifies the manufacturer, who is responsible for making sure that no two network adapters have the same MAC address.
 - Every device on a network (for example, computers, printers, smart thermostats, refrigerators, and smartphones) connects to the network by way of its NIC and its MAC address

**Misc**

**Host Name** - A host name or computer name identifies a host and can be used in place of its IP address on the local network. The name can have up to 63 characters, including letters, numbers, and special characters. Examples of computer names are www, ftp, JeanAndrews, TestBox3, and RedLaptop. You can assign a computer name while installing Windows. In addition, you can change the computer name at any time using the About window in the Settings app. See Figure 7-3.

**Domain Name** - A domain name identifies a network. Examples of domain names are the names that appear before the period in [microsoft.com](http://microsoft.com), _cengage.com_, and mycompany.com. The letters after the period are called the top-level domain and tell you something about the domain. Examples are .com (commercial), .org (nonprofit), .gov (government), .edu (education), and .info (general use).

**Fully Qualified Domain Name** - A fully qualified domain name (FQDN) identifies a computer and the network to which it belongs. An example of an FQDN is _www.cengage.com_. The host name is _www_ (a web server), _cengage_ is the domain name, and _com_ is the top-level domain name of the Cengage network. Another FQDN is joesmith.mycompany.com.