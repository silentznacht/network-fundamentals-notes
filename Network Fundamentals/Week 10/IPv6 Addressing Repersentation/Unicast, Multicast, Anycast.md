|Type|Sends To|Example Use|Notes|
|---|---|---|---|
|**Unicast**|One specific device|Device-to-device communication|Unique address|
|**Multicast**|Many selected devices|Routing updates, media streams|Replaces broadcast|
|**Anycast**|The nearest device with that address|DNS, CDNs, routing|Uses unicast format|


**Unicast** - An IPv6 unicast address uniquely identifies an interface on an IPv6 enabled device.
- **Definition:**  
	- A **unicast address** identifies **one single interface** (device connection) on a network. When you send a packet to a unicast address, **only that one device** receives it.

	- **Think of it like:**  
		📬 Sending a letter to one person’s exact home address.
	
	- **Example use:**  
	- When your computer talks directly to a web server, it uses **unicast**. Multicast - An IPv6 multicast address is used to send a single IPv6 packet to multiple destinations.

**Multicast**
- **Definition:**  
	- A **multicast address** sends **one packet** to **multiple specific devices** at once — not everyone, just members of that group.

- **Think of it like:**  
	📢 Sending one message to everyone in a group chat (not the entire phonebook).

- **Example use:**  
	- Used for things like streaming video or routing updates where multiple devices need the same info.

---

**Anycast**

**Definition:**  
An **anycast address** looks like a **unicast address**, but it’s **shared by multiple devices**.  
When a packet is sent to an anycast address, it’s automatically delivered to the **nearest** device (based on network distance).

**Think of it like:**  
📍 Mailing something to a chain store — it automatically goes to the _closest branch_.

**Example use:**  
Content delivery networks (CDNs), DNS servers, or load balancing between multiple routers.

**Note:**  
There’s a special multicast address in IPv6 called the **“All Nodes” multicast address**, which works kind of like IPv4’s broadcast — it reaches all IPv6-enabled devices on the local network.

Unlike IPv4, IPv6 does not have a broadcast address. However there is an IPv6 add nodes multicast address that essentially gives the same result.