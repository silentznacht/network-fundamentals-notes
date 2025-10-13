Simplified - The amount of bits locked in subnetmask ie 255.255.255.0 = 24 locked bits ~ each locked octet equals 8 locked bits 

Expressing network addresses and host addresses with the dotted decimal subnet mask address can become cumbersome. Fortunately, there is an alternative method of identifying a subnet mask, a method called the prefix length.

The prefix length is the number of bits set to 1 in the subnet mask. It is written in “slash notation”, which is noted by a forward slash (/) followed by the number of bits set to 1. Therefore, count the number of bits in the subnet mask and prepend it with a slash.

**Note:** A network address is also referred to as a prefix or network prefix. Therefore, the prefix length is the number of 1 bits in the subnet mask.

When representing an IPv4 address using a prefix length, the IPv4 address is written followed by the prefix length with no spaces. For example, 192.168.10.10 255.255.255.0 would be written as 192.168.10.10/24.
- (Prefix length is just the amount of bits that are locked, in this case 24 bits are locked, due to each octet (255) being locked and worth 8 bits, since 3 octets are locked then in total it will be 24 bits locked hence /24) 
- 192.168.10.10/24 - this means the ip addresses subnet mask has 24 locked bits.
