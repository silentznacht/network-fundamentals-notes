

##### TCP/IP Model Has Four Layers of Communication

Layer 4: Application layer
- Application-to-application communication is managed by the OS, using protocols specific to the application (HTTP, Telnet, FTP, and so forth). This layer of communication happens after the OSs have made a connection at the Transport layer.
Layer 3: Transport layer: Port addresses
- Host-to-host communication, managed by the OS, primarily using TCP and UDP protocols.
Layer 2: Internet layer: IP addresses
- Host-to-host on the local network or network-to-network communication, managed by the OS and network devices.
Layer 1: Link layer: MAC addresses
- Device-to-device on the local network, managed by firmware on NICs. Layer 1 is also called the Network interface layer or Network access layer.

- **Source Step 1: Application layer.** Recall that most applications that use a network are client/server applications. When a browser client makes a request to a web server, the browser passes the request to the OS. The OS formats the message using the appropriate application protocol (for example, HTTP, FTP, Telnet, DNS, and SSH). In our example, an HTTP message is created and passed down in the TCP/IP stack of protocols to the Transport layer.
	-  Notes:
		- Every modern operating system now has the TCP/IP model embedded into its kernel, to determine what protocols to use for an application ie (HTTP, Telnet, FTP, and so forth).
    
- **Source Step 2: Transport layer.** The Transport layer adds information to the message to address the correct server application. Depending on the type of application, the protocol TCP (Transmission Control Protocol) or UDP (User Datagram Protocol) adds the port assigned to the server application (TCP uses port 80 for HTTP communication in our example). The message with Transport data added is then passed down to the Internet layer.
	- Notes:
		- Hey if you arent understanding what this means above me, this is the simplified version.
			- Adds the **source and destination ports** (e.g., port **80** for HTTP). 
			- Uses **TCP** for reliable delivery or **UDP** for faster, simpler delivery.
			- Ensures the data reaches the correct application on the server.
    
- **Source Step 3: Internet layer.** The Internet layer is responsible for getting the message to the destination computer or host on the local network, an intranet, or the Internet. **An intranet is any private network that uses TCP/IP protocols**. A large enterprise might support an intranet that is made up of several local networks. The primary protocol used at the Internet layer is IP (Internet Protocol), which uses an IP address to identify each host. (Other Internet layer protocols include EIGRP, OSPF, BGP, and ICMP.) IP adds address information to the message and then passes it down to the Link layer.

- **Source Step 4: Link layer.** The Link layer is the physical network, including the hardware and its firmware for every device connected to the network. A computer’s network interface card (NIC) is part of this physical network. As you know, each NIC is able to communicate with other NICs on the local network using each NIC’s MAC address. For a local network, the physical connection might be wireless (most likely using Wi-Fi) or wired (most likely using Ethernet). The NIC receives the message from IP, adds information for Ethernet or Wi-Fi transmission, and places the message on the network.
    
- **Step 5: Network transmission.** IP at the Internet layer is responsible for making sure the message gets from one network to the next until it reaches its destination network (see Figure 7-5) and destination computer on that network. Whereas a MAC address at the hardware Link layer is only used to find a computer or other host on a local area network (LAN), an IP address can be used to find a computer on a local network, anywhere on the Internet (see Figure 7-6), or on an intranet.