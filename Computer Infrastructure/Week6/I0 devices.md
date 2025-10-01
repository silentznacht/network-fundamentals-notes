- All **I/O** or **storage device** can be either internal (installed inside the computer case) or external (installed outside the case and called a peripheral device).
	- when you install a new device, such as a webcam you must install both the device and drivers for the device. These drivers drives must be written for the OS (operating system your using).
		-  **Quick Note** - Recall from earlier modules that the exceptions to this principle are some simple devices, such as the keyboard, which are controlled by the system BIOS/UEFI. Also, Windows has embedded device drivers for many devices. For example, when you install a video card, Windows can use its embedded drivers to communicate with the card, but to use all the features of the card, you can install the drivers that came bundled with it or download the drivers from the manufacturer’s website.
	- install only one device at a time
	- use an adminstrative account when installing new devices
		-  because you need highest privilages to change system
	- often any problems with a device can be solved by updating it's driver (software)
	- a device is only as fast as it's designed to be using. 
		- An external hard drive designed to use a USB 2.0 port will work using a USB 3.0 port, but it will work at the USB 2.0 speed even when it’s connected to the faster USB 3.0 port.
	- **Quick Note**
		- Recall that Device Manager (its program file is named devmgmt.msc) is your primary Windows tool for managing hardware. It lists almost all installed hardware devices and the drivers they use. (Printers and many USB devices are not listed in Device Manager.) Using Device Manager, you can disable or enable a device, update its drivers, uninstall a device, and undo a driver update (called a driver rollback).

**USB and Connectors**
- As many as 127 USB devices can be daisy-chained together using USB cables. In a daisy chain, one device provides a USB port for the next device.
- USB uses serial transmissions, and USB devices are hot-swappable, meaning that you can plug in or unplug one without first powering down the system.
- A USB cable has four wires, two for power and two for communication. The two power wires (one is hot and the other is ground) allow the host controller to provide power to a device. Four general categories of USB ports and connectors are USB-C, regular USB, micro USB, and mini USB. Mini USB connectors are smaller and more durable than micro USB, which are smaller than regular USB connectors. USB4 only uses USB-C connectors. Table 6-2 shows the different USB connectors on USB cables.

**Video Connectors and Ports**

- Video ports are provided by a video card or the motherboard.

- Video cards are sometimes called graphics adapters, graphics cards, or display cards. Most motherboards sold today have one or more video ports integrated into the motherboard and are called onboard ports.

	- If you are buying a motherboard with a video port, make sure that you can disable the video port on the motherboard if it gives you trouble. You can then install a video card and use its video port rather than the port on the motherboard. Recall that a video card can use a PCI or PCI Express slot on the motherboard. The fastest slot to use is a **PCIe ×16 slot**.

**Simplified Notes**
- A **GPU should always go in the PCIe ×16 slot**, since that’s where it gets the most bandwidth and best performance.
    
- The **motherboard’s video ports** only work if the CPU has integrated graphics (like an Intel chip with an iGPU or an AMD APU).
    
- Integrated graphics (iGPU/APU) are fine for **basic tasks** (web browsing, office work, video playback), but they’re not designed for heavy gaming or demanding 3D work. That’s where a dedicated GPU is far superior.

	Many modern motherboards come with video output ports, but these only work if the CPU has integrated graphics. If you install a dedicated graphics card (GPU), you should use the video ports on the GPU instead, since they offer better performance. Sometimes the onboard video can cause conflicts, in which case you can disable it in the UEFI/BIOS or in the Windows Device Manager. Dedicated GPUs connect through PCI Express (PCIe) slots, and the fastest slot to use is the PCIe ×16 slot. The “×16” refers to the number of data lanes available—like lanes on a highway, more lanes mean higher bandwidth for data transfer between the GPU, CPU, and memory. A PCIe ×16 slot has 16 lanes working in parallel, giving the best possible performance for modern graphics cards, which is why you should always install the GPU in the primary ×16 slot on the motherboard.


	**Video Port Types:**
		- **VGA** 
			- The 15-pin VGA port is the standard analog video port and transmits three signals of red, green, and blue (RGB). A VGA port is sometimes called a DB-15 port.
		- **DVI Ports** (Designed to replace VGA)
			- DVI-D 
				-  Only transmits data, won't work with VGA adapter.Only supports digital data signal.
			- DVI-I
				- Supports both analog and digital signals,
				- Analog data is transmitted using the extra four holes on the right side of the connector.
		- **Display Port** (Designed to replace DVI)
		 		- Can transmit digital video and audio data
		 		- BIOS screen where you can enable or disable the audio transmissions of DisplayPort and HDMI ports and still use these ports for video.
		- **HDMI**
			- HDMI transmits both digital video and audio, and it was designed to be used by home theater equipment.
			- The HDMI standards allow for several types of HDMI connectors. The best known, which is used on most computers and televisions, is the Type A 19-pin HDMI connector.
		- **Thunderbolt**
			- Thunderbolt is a multipurpose connector used to connect high-end displays and external storage devices and to provide power for smartphones and laptops .
				- Earlier versions of Thunderbolt were limited to Apple products and used the DisplayPort base connection. The latest two versions, Thunderbolt 4 and Thunderbolt 3, use the USB-C connection (marked with a lightning bolt symbol), which opens the compatibility of Thunderbolt connections to non-Apple products.
		- **eSATA**
			- The eSATA port is used for connecting **external** storage devices to a computer
		- **RS-232**
			- USB or other connectors have replaced the serial RS-232 connectors once used with mice, keyboards, dial-up modems, and peripheral connections.
				- However, you might see a serial RS-232 connector on a rack server to set up a terminal to access the server. An earlier version of RS-232 had a 25-pin connector, but all RS-232 connectors today use nine pins and are often called DB-9 connectors