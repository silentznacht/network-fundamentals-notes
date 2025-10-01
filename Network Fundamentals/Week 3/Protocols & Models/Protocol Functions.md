**What are Protocol Functions?**
Network communication protocols are responsible for a variety of functions necessary for network communications between end devices. They are the subtasks or operations inside a protocol. They exist to help the protocol accomplish it's purpose, which is defined by the networks model layer. Each function is like a small step or mechanism that, combined with the other functions, lets the protocol do its job.


**Functions**


**Addressing ->** 

Addressing is a subtask of a protocol that ensures data reaches the correct destination. The sender **attaches its own address** (source address) and the **recipient’s address** (destination address) using a **defined addressing scheme**—a standardized format that all devices on the network understand. The receiver **checks the destination address** to confirm the message is meant for it and can use the source address if it needs to send a reply. **Examples Below:**
	- IPv4
	- IPv6
	- Ethernet

**Tip:** The “defined addressing scheme” just means that all devices **agree on the format and rules for addresses**, like IPv4, IPv6, or Ethernet MAC addresses, so communication works reliably. The **format** defines how the address looks (for example, IPv4 uses four numbers separated by dots, IPv6 uses hexadecimal numbers with colons, and Ethernet uses hexadecimal pairs separated by colons). The **rules** ensure each address is unique and interpreted the same way by all devices, so data is sent to the correct destination.

**Reliability->** This functions just guarenteeds delivery in case a message is lost or corrupted in transit. TCP provides guarenteed delivery.

**Flow Control->** This function ensures that data flows at an efficent rate between two communicating devices. 

**Error Detection->** This is used to determine if data has become corrupted during transmission. 

***Application Interface->*** This function contains information used for commincation between network applications, examples are a device tries to access a web page and HTTP or HTTPS protocols are used to communicate between the client and server web process.