
- **Store-and-forward switching** - This frame forwarding method receives the entire frame and computes the CRC. CRC uses a mathematical formula, based on the number of bits (1s) in the frame, to determine whether the received frame has an error. If the CRC is valid, the switch looks up the destination address, which determines the outgoing interface. Then the frame is forwarded out of the correct port.

**Simplified:**
	This method recieves a frame, then uses CRC (a mathamatical equation) to determine if the recieved frame has an errors. If there are no detected errors, then it will check the frames destination MAC address.  Then checks it MAC address table, and forwards the frame to the correct port.
		Positives:  Error detection helps reduce corrupted data that consumes unusued bandwidth.
			- Required for QoS networks.

- **Cut-through switching** - This frame forwarding method forwards the frame before it is entirely received. At a minimum, the destination address of the frame must be read before the frame can be forwarded.

**Simplified**:
	This methods forwards a frame before fully recieving it, just reading the destination address, and getting sent to the correct port.