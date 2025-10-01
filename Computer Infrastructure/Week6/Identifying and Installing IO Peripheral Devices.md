
IO Periphal Devices = External devices, like a webcam. Which require drivers that essentially allow the peripheral io device and os to communicate with each other, windows often has many compatiable drivers for all peripheral devices. Drivers are essentially the software made specifically for that device that allow communication between both peripheral device and OS.


- Simple input devices like a mouse or keyboard don't require drivers, because the OS often is embedded natively with drivers built in for these devices.

**Steps**

- **Read the manufacturer’s directions.** I know you don’t want to hear that again, but when you follow these directions, the installation goes smoother. If you later have a problem with the installation and you ask the manufacturer for help, being able to say you followed the directions exactly as stated goes a long way toward getting more enthusiastic help and cooperation.
    
- **Make sure the drivers provided with the device are written for the OS you are using.** Recall that 64-bit drivers are required for a 64-bit OS, and 32-bit drivers are required for a 32-bit OS. You can sometimes use drivers written for older Windows versions in newer Windows versions, but for best results, use drivers written for the OS installed. You can download the drivers you need from the manufacturer’s website.
    
- **Make sure the motherboard port you are using is enabled.** It is most likely enabled, but if the device is not recognized when you plug it in, go into BIOS/UEFI setup and make sure the port is enabled. In addition, BIOS/UEFI setup might offer the option to configure a USB port to use USB4, SuperSpeed+ (USB or 3.2 or 3.1), SuperSpeed (USB 3.0), Hi-Speed USB (USB 2.0), or original USB (USB 1.1). Refer back to Figure 6-6, which shows the BIOS setup screen for one system where you can enable or disable onboard devices. In addition, if you are having problems with a motherboard port, don’t forget to update the motherboard drivers that control the port.
    
- **Install drivers or plug in the device.** Some devices, such as a USB printer, require that you plug in the device before installing the drivers, and some devices require you to install the drivers before plugging in the device. For some devices, it doesn’t matter which is installed first. Carefully read and follow the device documentation. For example, the documentation for one scanner says that if you install the scanner before installing the drivers, the drivers will not install properly.
    
    If you plug in the device first, Device Setup launches and steps you through the installation of drivers (see Figure 6-13). As Device Setup works, an icon appears in the taskbar. To see the Device Setup dialog box, as shown in the figure, click the icon.

- If you need to install the drivers first, run the setup program on CD or DVD. If you downloaded drivers from the web, double-click the driver file and follow the directions on-screen. It might be necessary to restart the system after the installation. After the drivers are installed, plug the device into the port. The device should immediately be recognized by Windows. If you have problems using the device, turn to Device Manager for help.
    
- **Install the application software to use the device.** For example, a USB camcorder is likely to come bundled with video-editing software. Run the software to use the device.


**Mouse and Keyboard**

- When you plug in a mouse or keyboard, windows should immediately recognize the devices, and install the generic drivers.
	- Older computers used PS/2 ports for the mouse and keyboard. Because these ports were not hot-pluggable, you had to restart Windows after plugging in a mouse or keyboard.
- You can use Device Manager to uninstall, disable, or enable most devices. However, USB devices are managed differently.
	- To uninstall a USB device such as a USB graphing tablet, use the Programs and Features window or the Apps & features window.
		- To open the Windows 10 Apps & features window, right-click the **Start** button, select **Apps and Features**, and then select the device and click **Uninstall**.


**Web Camera**

- A webcam (web camera) is embedded in most laptops and can also be installed as a peripheral device using a USB port or some other port.
	- First install software then plug in the webcam
- Comes with a built-in microphone

**Graphics Tablets**

- Another input device is a **graphics tablet,** also called a **digitizing tablet or digitizer**, which is used to hand draw.
- Likely to connect to a usb port
- Comes with a **stylus** that works like a pencil on the tablet and controls the pointer on the screen
- The graphics tablet and stylus can be a replacement for a mouse or touch pad on a laptop, and some graphics tablets come with a mouse. Graphics tablets are popular with graphic artists and other content creators who use desktop publishing applications.
- Install the graphics tablet the same way you do other USB devices. Additional software might be bundled with the device to enhance its functions, such as inputting handwritten signatures into Microsoft Word documents.