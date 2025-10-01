
The processor installed on a motherboard is the primary component that determines the computing power of the system.



**The  features of a processor that affect performance and compatibility with motherboards**

- **Feature 1: Processor speed.** The processor frequency is the speed at which the processor operates internally and is measured in gigahertz, such as 3.3 GHz. Current Intel and AMD processors run from about 2.0 GHz up to more than 5.3 GHz.
    
- **Feature 2: Lithography.** The lithography is the average space between transistors printed on the surface of the silicon chip. The measurement is in nanometers (nm); 1 nm is 1 billionth of a meter. Current processor lithography ranges from 7 nm to 14 nm. The lower the measurement, the better and faster the processor performs.
    
- **Feature 3: Socket and chipset the processor can use.** Recall that current Intel sockets for desktop and server systems are LGA1700, LGA1200, LGA1151, LGA2066, and LGA2011. AMD’s current desktop sockets are sTRX4, TR4, AM4, AM3+, AM3, and FM2+.
    
- **Feature 4: Multiprocessing abilities.** The ability of a system to do more than one task at a time is accomplished by several means:
    
    - **Multiprocessing.** Using two processing units (called arithmetic logic units or ALUs) installed within a single processor is called multiprocessing. With multiprocessing, the processor, also called the core, can execute two instructions at the same time.
        
    - **Multithreading.** Each processor or core processes two threads at the same time. When Windows hands off a task to the CPU, it is called a thread and might involve several instructions. To handle two threads, the processor requires extra registers, or holding areas, within the processor housing that it uses to switch between threads. In effect, you have two logical processors for each physical processor or core. Intel calls this technology Hyper-Threading and AMD calls it HyperTransport. The feature must be enabled in BIOS/UEFI setup, and the operating system (OS) must support the technology.
        
    - **Multicore processing.** A single processor in the processor package is called single-core processing, and using multiple processors installed in the same processor housing is called multicore processing. Multicore processing might contain up to 32 cores (dual-core, triple-core, quad-core, and so forth). In Figure 3-2, the quad-core processor contains four cores or CPUs. Using multithreading, each core can handle two threads. Therefore, the processor appears to have up to eight logical processors, as it can handle eight threads from the operating system.