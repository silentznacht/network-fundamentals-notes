Different physical media support the transfer of bits at different rates. Data transfer is usually discussed in terms of bandwidth. **Bandwidth is the capacity at which a medium can carry data**. Digital bandwidth measures the amount of data that can flow from one place to another in a given amount of time. Bandwidth is typically measured in kilobits per second (kbps), megabits per second (Mbps), or gigabits per second (Gbps). Bandwidth is sometimes thought of as the speed that bits travel, however this is not accurate. For example, in both 10Mbps and 100Mbps Ethernet, the bits are sent at the speed of electricity. The difference is the number of bits that are transmitted per second.

A combination of factors determines the practical bandwidth of a network:

- The properties of the physical media
- The technologies chosen for signaling and detecting network signals

Physical media properties, current technologies, and the laws of physics all play a role in determining the available bandwidth.

![[Screenshot 2025-09-05 at 22-58-33 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

# **Terminology**

Terms used to measure the quality of bandwidth include:
- Latency
- Throughput
- Goodput

**Latency** = Latency is the time it takes for data to travel from one point to another. In a network, the overall speed is limited by the slowest part of the path, so even if most connections are fast, a single slow link can create a bottleneck.
A **bottleneck** is the part of a network (or system) that **slows down the overall data flow**

**Throughput** = The actual amount of data transferred over a network in a certain time. It is usually **less than the maximum bandwidth** because of traffic, network delays, and device processing.

**Goodput** = The portion of throughput that is **useful data**. It excludes overhead like acknowledgments, retransmissions, and protocol headers, so it’s always **less than throughput**. Goodput is throughput minus traffic overhead for establishing sessions, acknowledgments, encapsulation, and retransmitted bits. Goodput is always lower than throughput, which is generally lower than the bandwidth.

- **Throughput** = All data being sent over the network, including extra bits like headers, acknowledgments, and retransmissions.
    
- **Goodput** = Only the **useful, meaningful data** that the recipient actually needs, excluding all the extra overhead.