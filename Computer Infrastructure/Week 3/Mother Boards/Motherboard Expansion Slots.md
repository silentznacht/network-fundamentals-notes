
 ![[comp_bus.png]]

The expansion slots use an expansion bus, to connect those additional components to the rest of the motherboard. 

**Expansion Bus**
	-  "Width" in bits
	-  Big roads, little roads
	-  Width is changing bandwidth
- The wider the bus the more information we are allowed to send


**Conventional PCI**
	- Peripheral Component Interconnect
	-  PCI interface cards communicate over a parrallel connection and will support a 32 bit or 64 bit parrallel  communication.
	![[Screenshot 2025-08-30 at 21-52-16 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term).png]]

**PCI 32-bit and 64 bit slots** 
![[Screenshot 2025-08-30 at 21-57-58 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term) 1.png]]

**NOTE**: Just so you dont confuse yourself, PCI slots and expansion slots are not the same. An expansion slot is the general connector on the motherboard that lets you add extra parts like graphics cards, sound cards, or network cards. A PCI (Peripheral Component Interconnect) slot is one specific type of expansion slot that was popular in older computers. Over time, different standards have been used: ISA (very old), then PCI, then AGP for graphics, and now PCI Express (PCIe), which is the modern standard. In short: _all PCI slots are expansion slots, but not all expansion slots are PCI_. Expansion slot = the category, and PCI = one older version inside that category.

Expansion slot is just the broad term,  ISA, PCI, AGP, PCIe, etc are just terms explaining the slot technology.

- **ISA** → really old, slow.
- **PCI** → replaced ISA, became the standard in the 90s/early 2000s.
- **AGP** → special slot only for graphics cards (now obsolete).    
- **PCIe (PCI Express)** → today’s standard, much faster and flexible.

The shorter slots are the 32 bit slots, and the larger slots are the 64 bit slots. The notes or keys on the PCI slots determine the type of card that will connect to these different interfaces.


**PCI Expansion Card** - 32 Bit
![[Screenshot 2025-08-30 at 22-12-31 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term).png]]
**PCI Expansion Card** - 64bit![[Screenshot 2025-08-30 at 22-19-01 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term).png]]

- These PCI expansion cards are placed in the PCI expansion slot.
- PCI cards get power directly from the **PCI slot** itself (the motherboard provides the needed voltage).
- As shown in the image, the PCI slot will have to provide power at 3.3V or 5V


**PCI Express (PCIe)**

Note: PCIe has essentially replaced all of the older expansion slot types
![[Screenshot 2025-08-30 at 22-21-48 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term).png]]

**PCIe Express Serial Connection**

**Note:** 

Older **PCI slots** used a **shared parallel bus**, meaning all devices shared the same set of data lines, sending many bits at once. This design ran into limits like **clock skew** (timing issues between lines) and devices having to wait their turn, which slowed things down.

Modern **PCI Express (PCIe)** fixed this by using **high-speed serial point-to-point links**. Each device gets its own **dedicated lane(s)**, sending data one bit at a time but at very high speeds. Because lanes can be combined (x1, x4, x8, x16), PCIe is both **faster and more scalable** than PCI. 
![[Screenshot 2025-08-30 at 22-34-31 Week 3 COMPUTING INFRS (CTS1131C - 20159 - Full Term).png]]
