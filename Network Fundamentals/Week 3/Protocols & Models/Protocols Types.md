You know that for end devices to be able to communicate over a network, each device must abide by the same set of rules. These rules are called protocols and they have many functions in a network. This topic gives you a overview of network protocols.

Network protocols define a common format and set of rules for exchanging messages between devices. Protocols are implemented by end devices and intermediary devices in software, hardware, or both. Each network protocol has its own function, format, and rules for communications.

The table lists the various types of protocols that are needed to enable communications across one or more networks.

**Protocol Types**

**Network Communication Protocols -**** This protocol enables two or more devices to communicate with each other over one or many other networks. Technologies that involves these sorts of protocols are under the Ethernet family. **Such as the following below**
		-  IP
		-  Transmission Control Protocol (TCP)
		- etc


**Network Security Protocols -**  This protocol essenitally secures data to provide things like authentication, data integrity, and data encryption. **Examples of secure protocols are listed below:**

-  **Secure Shell (SSH) ->** A secure encrypted method to access devices over a network
-  **Secure Sockets Layer(SSL) ->** Creates an encrypted link between a webserver and a brower
	-  Encrypts important information like usernames, passwords, credit card details, sensitive information, etc.
-  **Transport Layer Security (TLS)->** This is essentially a cryptographic protocol that encrypts data when in transit to ensure the privacy of communication between a client and server. **The process is explained below:** 
	- **Client Hello**
	    - Browser (client) sends a request to start TLS.
            Includes supported cipher suites (encryption algorithms), TLS version, and a random number.
	-  **Server Hello**
		- Server responds with its chosen cipher suite, its own random number, and its digital certificate (issued by a trusted Certificate Authority).
	- **Certificate Verification**
		- Browser checks the server’s certificate to ensure:
		- It’s signed by a trusted CA.
		- It hasn’t expired.
        - The domain matches.
	- **Key Exchange**
	    - Depending on the method (RSA, Diffie-Hellman, ECDHE), the browser and server establish a **shared session key**.
	    - With forward secrecy (e.g., ECDHE), each session gets a new unique key.
	- **Session Keys Established**
	    - Both sides now have the same symmetric session key, used for encrypting/decrypting data.    
	    - From this point onward, all communication is encrypted.
	        

---
**Routing Protocols -** This enables routers to exchange route information, and compare path information, to determine the best path to the destination network. Examples of this protocol is below:

	- Open Shortest Path First (OSPF)
	- Border Gateway Protocol (BGP)


**Service Discovery Protocols -**  This protocol is used to automatically detect devices or services. **Examples of this are below:**
	- **Dynamic Host Configuration Protocol (DHCP)->** Automatically assigns IP addresses and network configurations to devices, when they are connected to a network.
	- **Domain Name System (DNS) ->** Acts as a internet phone book translates domain names into machine readbale IP address (e.g., google.com -> 172.217.160.142).
	   IP addresses are already assigned to servers by whoever manages the hosting/network (e.g., hosting provider, ISP, or system admin). DNS is essenitally just a middle man, it translates a human-friendly domain name, and matches it with the IP Address that matches it. Then it points the direction, and tells your browser where to send you.
