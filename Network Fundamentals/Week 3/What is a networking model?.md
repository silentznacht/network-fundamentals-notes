
**Network Protocol (ie OSI or TCP/IP)*

- Networking models categorize and provide structure for networking protocols and standards.
- A networking protocol (like TCP/IP) is a set of rules defining how devices and software should work, including how they should work together.

		**Protocols**
				- Protcols refer to logical rules, on how devices should
				 communicate, not physical standards.



**OSI Model - Layer 7 (Application)**

- The application layer (layer 7) is the layer that is closest to the end user.
- The application layer interacts with software applications that have some communication component, such as a web browser (fire fox, chrome, brave etc)
	- For example, HTTP and HTTPS are Layer 7 protocols
	- Exmp -> (https://www.cisco.com) -> this indicates that HTTPs is being used to get to this website and view it in the browser
	- **Clarification**:  In layer 7 the applications themselves arent included in the layer, but rather protocols that interact with the application like HTTP and HTTPS
- Some functions of Layer 7:
	- Identifying communication partners 
	- Synchronizing communication

**OSI Model - Layer 6 (Presentation)**
	- The presentation layer's (layer 6) job is to translate between the application and network formats, this is due to the data in an application layer (layer 7) is in an "application format", it needs to be translated to a different format so that it can sent over a network. 
		- For example, encryption of data as it is sent, and decryption data as it is received.
	- To summarize, the presentation  layer (layer 6) translates data to the appropriate format

**OSI Model - Layer 5 (Session)**
	- The session layer controls dialogues, also known as "sessions", between communicating hosts.
	-  It establishes manages, and terminates connections between the local application (for example, web browser) and the remote application (for example youtube).
	- Think of it as the **“conversation manager”** — making sure two applications can talk, pause, resume, and close properly.


**Upper Layers**
![[Screenshot 2025-09-05 at 19-07-55 (605) Free CCNA OSI Model & TCP_IP Suite Day 3 CCNA 200-301 Complete Course - YouTube.png]]

**Note *Encapsulation*:**

 Data is prepared in the top 3 layers (application, presentation, session) is sent down to the bottom 4 layers (transport, network, data link, physical) which actually does the job of sending out that data over the network.  After the top 3 layers hand data over to the bottom 4 layers, the next step before sending data is that the **transport layer (layer 4)** adds a header in front of the data.
![[Screenshot 2025-09-05 at 19-14-44 (605) Free CCNA OSI Model & TCP_IP Suite Day 3 CCNA 200-301 Complete Course - YouTube.png]]

**OSI Model - Layer 4 (Transport)**
	- Segments and reassembles data for communication between end hosts.
	- It breaks large pieces of data into smaller segments which can be more easily sent over the network and are less likely to cause transmission problems if errors occur. 

**OSI Model - Layer 3 (Network)**
	- Provides connectivity between end hosts on a different networks (ie. outside of the LAN)
	- The network layer allows communication **beyond the local network (LAN)**.
	- Provides logical addressing (IP addresses)
	- Provides path selection between source (SRC) and destination (DST)
	- **Routers** operate at Layer 3


**Note: Encapsulation Process**

Data is prepared by the upper layers, the transport layer adds a layer 4 header, and this combination of data plus a layer 4 header is called a **segment**. Next network layer adds a layer 3 header, including information like the source and destination IP address to the segment. This combination of data, layer 4 header and layer 3 header is called a packet. Then the packet is further encapsulated at Layer 2, this time with both a layer 2 header and a layer 2 trailer.

 **Header** → Contains the source and destination **MAC addresses**.
**Segment** = Data (data prepared from upper layers) + layer 4 header 
**Packet** = **Segment** (Data + layer 4 header) + **layer 3 header**
**Frame** = **Packet** + Layer 2 header + Layer 2 trailer

**OSI Model - Layer 2 (Data Link)**
	- Provides node to node connectivity and data transfer (for example, PC to switch, switch to router, router to router)
		- Example:
		****	- A **PC to a switch** (the switch ensures the data goes to the correct device).
			- A **switch to another switch** in the same LAN.
		- Think of it as **local delivery**, like a mail carrier delivering letters only within the same neighborhood, before Layer 3 (Network) takes over for long-distance delivery.
- A **router to another router** (when they’re directly connected via Ethernet).
	- Defines how data is formatted for transmission over a physical medium (for example, copper UTP cables)
	- Detects and possibly corrects physical layer errors
	- Uses layer 2 addressing, seperate from layer 3 addressing
	- **Switches** operate at layer 2
		- Switches look at the destination layer 2 address to determine where to send the data
		
**OSI Model - Layer 1 (Physical Layer)**
	- Defines physical characteristics of the medium to transfer data between devices.
	- For example, voltage levels, maxium transmission distances, physical connectors, cable specifications, etc
	- Digital bits are converted into electrical signals for wired connections, or radio signals for wireless connections

- - Deals with the actual hardware and physical means of sending data.
    
- Includes cables, connectors, voltage, distances, and other specifications.
    
- Converts digital bits into electrical signals (wired) or radio signals (wireless).


**OSI Model Simplified (Layer 7 → Layer 1)**

**Layer 7 – Application**

- Directly interacts with users and applications.
    
- Examples: web browsing, email, file transfer.
    

**Layer 6 – Presentation**

- Prepares data for the application layer.
    
- Handles encryption, compression, and formatting.
    

**Layer 5 – Session**

- Manages and maintains communication sessions between devices.
    
- Example: your browser connecting and staying connected to a server.
    

**Layer 4 – Transport**

- Ensures reliable delivery of data between devices.
    
- Splits data into segments and reassembles them.
    
- Protocols: TCP (reliable), UDP (fast).
    

**Layer 3 – Network**

- Moves data across different networks.
    
- Uses IP addresses to find the best path.
    
- Routers work here.
    

**Layer 2 – Data Link**

- Connects devices on the same network.
    
- Uses MAC addresses to identify devices.
    
- Detects and sometimes corrects errors from the physical layer.
    

**Layer 1 – Physical**

- Handles the actual hardware and signals.
    
- Deals with cables, connectors, voltage, distances.
    
- Converts bits into electrical or radio signals.