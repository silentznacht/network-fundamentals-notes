![[Screenshot 2025-09-06 at 10-05-26 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

### **Unshielded twisted-pair (UTP)**

**UTP is the most common cabeling in networking media(Ethernet LANs, telephone systems)**. UTP cabeles are terminated (executed) **with RJ-45 connecters**(connector on end of cable, used to connect to a device), these two are used for interconnecting network hosts with intermeditary networking devices, like switches and routers.
	- **Termination**: Uses **RJ-45 connectors** to connect end devices (PCs, printers) and networking devices (switches, routers)
	- **Characteristics**:
		- Cheaper and easier to install than STP.
		- Relies on wire twisting to reduce **crosstalk** (signal interference between pairs).
		- More vulnerable to **EMI/RFI** (electromagnetic/radio frequency interference).

### **Shielded twisted-pair (STP)**

A shielded twisted-pair (STP) provides better noise protection than UTP cabling(meaning it wont be as easy to be interuppted or cause latency). But compared to UTP, STP is much more expensive and difficult to install. Much like UTP, STP also uses an RJ-45 connector.  

STP cables combine the techniques of shielding to counter EMI and RFI, and wire twisting to counter crosstalk. To gain the full benefit of the shielding, STP cables are terminated with special shielded STP data connectors. If the cable is improperly grounded, the shield may act as an antenna and pick up unwanted signals.

The STP cable shown uses four pairs of wires, each wrapped in a foil shield, which are then wrapped in an overall metallic braid or foil.
	- Designed to provide **better noise protection** than UTP.
	- **Termination**: Also uses **RJ-45 connectors**, but requires **special shielded connectors** for full effectiveness.
	- **Characteristics**:
		- **Shielding + twisting** help block interference:
	    - **Twisting** counters **crosstalk**.    
	    - **Shielding** (foil or braid) blocks **EMI/RFI**.
	    - More **expensive and harder to install** than UTP.
		- If **not grounded properly**, shielding can act like an antenna and attract interference instead of blocking it.
	- **Structure**:
		- Four twisted pairs.
		- Each pair may have its own foil shield.
		- All pairs are wrapped in an overall metallic braid or foil.

**UTP = Cheaper, easier, but less protection.**
**STP = More expensive, harder to install, but stronger against interference.**

### **Coaxial Cables**

Coaxial cable, or coax for short, gets its name from the fact that there are two conductors that share the same axis. As shown in the figure, coaxial cable consists of the following:

- A copper conductor is used to transmit the electronic signals.
- A layer of flexible plastic insulation surrounds a copper conductor.
- The insulating material is surrounded in a woven copper braid, or metallic foil, that acts as the second wire in the circuit and as a shield for the inner conductor. This second layer, or shield, also reduces the amount of outside electromagnetic interference.
- The entire cable is covered with a cable jacket to prevent minor physical damage.

There are different types of connectors used with coax cable. The Bayonet Neill-Concelman (BNC), N type, and F type connectors are shown in the figure.

Although UTP cable has essentially replaced coaxial cable in modern Ethernet installations, the coaxial cable design is used in the following situations:

- **Wireless installations** - Coaxial cables attach antennas to wireless devices. The coaxial cable carries radio frequency (RF) energy between the antennas and the radio equipment.
- **Cable internet installations** - Cable service providers provide internet connectivity to their customers by replacing portions of the coaxial cable and supporting amplification elements with fiber-optic cable. However, the wiring inside the customer's premises is still coax cable.![[Screenshot 2025-09-06 at 11-33-18 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

### **Electromagnetic Interference (EMI)**
-**What it is**: Unwanted disturbance caused by external electrical signals.
-**Causes**: Anything that gives off an electromagnetic field — examples: fluorescent lights, power lines, motors, elevators, large machinery.
-**Effect**: Can disrupt or degrade the signal traveling in a cable.

### **Radio Frequency Interference (RFI)**
-**What it is**: A specific type of EMI that comes from radio frequency sources.
-**Causes**: Wireless transmitters, cell towers, microwave ovens, radio/TV antennas.
-**Effect**: Similar to EMI — can interfere with wired signals, especially in poorly shielded cables.
**Key Distinction**
- **EMI/RFI** → external interference from the environment.
- **Crosstalk** → internal interference between wire pairs inside the cable.
### Why Twisting Helps
- In both UTP and STP, the **twisting** of wire pairs cancels out most crosstalk.    
- **Shielding** (in STP) helps block external EMI/RFI.