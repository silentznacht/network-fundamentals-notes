- Simplified - A subnet mask is used to identify the network and host portion of an IPv4 address. Each 255 repersents an octet of locked bits meaning it cannot vary or change, while 0 means it varies, for example 168.92.6.19 with the subnet mask of 255.255.0.0 means that 168.92 cannot change, their octets / bits are locked, meaning this is the network portion of the address, which is used to identify the network address ie the network the device/host is on, while 6.19 is the host portion that identifies where the device is in the network.

- **IPv4 address** - This is the unique IPv4 address of the host.
- **Subnet mask**- This is used to identify the network/host portion of the IPv4 address.

**Note:** **A default gateway IPv4 address is required to reach remote networks** and DNS server IPv4 addresses are required to translate domain names to IPv4 addresses.

**The IPv4 subnet mask is used to differentiate the network portion from the host portion of an IPv4 address**. When an IPv4 address is assigned to a device, the subnet mask is used to determine the network address of the device. The network address represents all the devices on the same network.
![[Screenshot 2025-10-11 at 19-05-18 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]
Note that the subnet mask does not actually contain the network or host portion of an IPv4 address, it just tells the computer where to look for the part of the IPv4 address that is the network portion and which part is the host portion.

The actual process used to identify the network portion and host portion is called ANDing.

**Note:** If you’ve ever wondered _“Why is it 255? Why all 1s?”_ — here’s the deal:  
Each `1` in the subnet mask represents a **locked bit**, meaning that part of the IP address **cannot vary**. This “locks” the network portion so it stays consistent across all devices in that subnet.
Only the bits represented by `0`s are **unlocked**, allowing those values to change — that’s where the unique host addresses come from.

In simple terms:

> The subnet mask “locks in” the network bits (the 255s) and lets the host bits (the 0s) vary — keeping the network organized and preventing chaos.