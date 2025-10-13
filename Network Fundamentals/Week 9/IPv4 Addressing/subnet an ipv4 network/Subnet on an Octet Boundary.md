Subnetting is the process of **dividing a larger IPv4 network into smaller, more manageable sub-networks** (subnets).

Why do we do this?

- **Limit broadcast traffic** → smaller subnet = fewer devices per broadcast domain → more efficient.
    
- **Organize networks** → group devices logically (departments, floors, etc.).
    
- **Control growth** → avoid wasting IP addresses in huge networks.

Simplified - In subnetting your extending the network portion of your network address, this how a large network exmp 192.68.0.0/16 255.255.0.0 can be segmented into smaller subnets ie 192.68.140.0/24, 192.68.102.0/24 etc. Your probably wondering how so? Well remember how earlier you learned how a subnet mask helps identifies a networks address, and in turn can lock octets in a network address, ie 255 = locked bits (locked octet or 8 locked bits), and 0 means the host portion can vary 0 - 255.

Well when segmenting a large network and creating a subnet what you are doing is extending those network bits ie network portion of a network address. This is how 192.68.0.0 can be segmented into subnets like 192.68.102.0 and 192.68.140.0. And if your wondering how so, its because in the original network address, it was 192.68.0.0, meaning its subnet mask held / locked 2 octets ie 16 bits while that last 2 octets were for the host portion of the address. But by extending the network bits by 8 bits, instead now the subnet mask for that smaller subnet will be 255.255.255.0, this is because instead of 2 octets being locked, now it is 3. This can vary as some subnets can take more than just 8 bits, or abit less, but the point is that subnetting requires the network address to extend its network portion. By doing this it makes each subnet unique. 

Oh and your probably wondering, if each octet is locked how can it go from 0 to something else; how can the new bits have a different number now? 

Well thats possible when your extending the network portion of the network address, this results in those network bits (in our case the third octet) to generate, because your borrowing them ie extending the network portion, resulting in a unique number for that octet to represent the subnet (0 - 255)

---
In the previous topic you learned several good reasons for segmenting a network. You also learned that segmenting a network is called subnetting. Subnetting is a critical skill to have when administering an IPv4 network. It is a bit daunting at first, but it gets much easier with practice.

IPv4 subnets are created by using one or more of the host bits as network bits. This is done by extending the subnet mask to borrow some of the bits from the host portion of the address to create additional network bits. The more host bits that are borrowed, the more subnets that can be defined. The more bits that are borrowed to increase the number of subnets reduces the number of hosts per subnet.
- Simplified: Basically to create an IPv4 subnet, the subnet mask has to borrow some bits from the network portion of the address ie 255.255.0.0 now 255.255.255.0, the more bits that are borrowed the less hosts can be in the subnet. 
- ![[Pasted image 20251013190814.png]]

Networks are most easily subnetted at the octet boundary of /8, /16, and /24. The table identifies these prefix lengths. Notice that using longer prefix lengths decreases the number of hosts per subnet.
