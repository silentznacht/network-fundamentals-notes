
RAID is an array of drives.

RAID is a method or system that dictates how multiple physical drives are organized to work together, providing improved performance, data redundancy, or both, depending on the RAID level used.

RAID 0 - Striping -> Splitting a file between 2 or more different drives -> high performance because you can write alittle bit of information to multiple drives simultaneously
		- High performance
		- No redundancy, a drive failure breaks the array
		- Lose all access to your data

RAID 1 - Mirroring -> writes exactly the same information from one drive to both drives creating a mirror
		- High disk utilization (alot of drive space used)
			- Every file is duplicated
			- Required disk space doubled
		 - High redundancy (No data loss)
			 -  Drive failure does not affect data availability
			 
RAID 5 -  Striping with Parity -> 

**RAID 5** uses **striping with distributed parity**. Data is split across all drives (striping) for speed, and with each “row” of data, one drive stores parity — special calculated information that can rebuild missing data if a single drive fails. The parity position rotates across drives, so no single disk is just for parity (e.g., in set one, Disk 3 holds parity, in set two, Disk 2 does, in set three, Disk 1 does, and so on). With at least three drives, RAID 5 provides both good read speed and fault tolerance: if one drive fails, the system reconstructs its data using the parity plus the remaining drives. However, if two drives fail at once, all data is lost.

- Stripe 1:
    
    - A = Data1
        
    - B = Data2
        
    - C = Parity (based on Data1 + Data2)
        
- Stripe 2:
    
    - A = Data3
        
    - B = Parity (based on Data3 + Data4)
        
    - C = Data4
        
- Stripe 3:
    
    - A = Parity (based on Data5 + Data6)
        
    - B = Data5
        
    - C = Data6


Nested RAID - RAID 1+0 (aka RAID 10)
	- A stripe of mirrors
	- and saving it 

Striping data across 3 or more drives 


There are two major types of RAID configurations

- Software Based RAID
		- A feature of an operating system
		- Doesn't require any special hardware
		- Usually lower performance than hardware based
		- Software RAID is essentially plug and play, it is already built          into the operating system, you can install multiple harddrives into your computer and tell your OS you'd like to use this drives as a RAID array.


- Hardware Based RAID
		- A feature of the hard drive controller
		- Configured outside of the OS
			- ususally invisible to operating system
		- High performance, designed for speeds
		- You'd configure all of your RAID configurations on the controller, and the OS sees this as all one single drive


Software based - inexpensive, lower performance
Hardware based - expensive, high performance

Hot Swappable Drives
	- Add and remove while the system is running
		- The connection is "hot"
	- Common in drive chassis (Two or more drives)
	- Easy to repair
		- Replace a drive while system is running
		- Combine with RAID for 100% uptime