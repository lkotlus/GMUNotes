### Transport Layer
- Our goals:
	- Understand principles behind transport layer services:
		- Multiplexing, demultiplexing
		- Reliable data transfer
		- Flow control
		- Congestion control
	- Learn about internet transport layer protocols:
		- UDP
		- TCP
			- TCP congestion control
- The application layer has APIs to the transport layer. This makes things easier for the grammers. 
- Roadmap:
	1. Transport-layer services
	2. Multiplexing and demultiplexing
	3. Connectionless transport (UDP)
	4. Principles of reliable data transfer
	5. Connection-oriented transport (TCP)
	6. Principles of congestion control
	7. TCP congestion control

#### Transport-layer services
- Transport services and protocols
	- These provide logical communication between application processing running on different hosts.
	- Actions in end systems:
		- Sender: breaks messages into segments, passes to network layer
		- Receiver: assembles segments into messages and passes to application layer
	- This makes sense.
	- Transport layer segments and network layer "datagrams" are typically just called packets.
- Transport vs. Network layer services and protocols:
	- Network layer: logical communication between hosts
	- Transport layer: logical communication between processes
		- Relies on and enhances network layer services
- The big two:
	- TCP (Transmission Control Protocol)
		- Reliable and in-order delivery
		- Congestion control
		- Flow control
		- Connection setup
	- UDP (User Datagram Protocol)
		- Speed
		- We don't need ordered delivery or reliability. Send it unordered and unreliable.
	- Neither UDP or TCP offer delay guarantees or bandwidth guarantees.
- Data encapsulation and the protocol stack:
	- Starting at the highest protocol, each protocol or service at each layer adds its own information to the data

#### Multiplexing and demultiplexing
- In a nutshell:
	- Gather data from multiple processes of the sender, envelope them with a header, and send them as a whole (multiplexing)
	- Send the received segments to the correct application layer processes. 
- Demultiplexing:
	- Host receives IP datagrams
		- Each datagram has source IP address and destination IP address
		- Each datagram carries one transport-layer segment
		- Each segment has source and destination port numbers
	- Host uses IP address and port numbers to direct segments to their appropriate sockets.
	- Connectionless Vs. Connection-oriented:
		- Connectionless just uses port number
		- Connection-oriented uses port number and IP address.

#### Connectionless transport (UDP)
- "Bare bones" internet transport protocol
- "Best effort" service, UDP segments may be:
	- Lost
	- Delivered out-of-order to application
- Typically used for:
	- Streaming apps
	- DNS
	- SNMP
- Each segment:
	- Source port, destination port, length, checksum, and application data.
- UDP exists because we want a fast way to send lots of data. We're more concerned with speed than data integrity.
- UDP checksum:
	- Goal is to detect errors in transmitted segment.
	- The sender:
		- Treats contents of UDP segments (including header fields) as a sequence of 16-bit integers
		- The checksum is the addition of all segment content
		- Checksum value is then put into UDP checksum field
		- This is fairly weak security, we can easily spoof a corrected checksum.
	- Receiver:
		- Compute the checksum
		- Check if the computed and received checksums are equal 
			- If not, there's an error
			- If equal, there may be an error, but we don't think there is one
	- If we get a 17-bit integer result, then we wraparound by adding it to the first one and carrying the consequences.
	- You then invert each bit in the sum, and that is your checksum.

#### Principles of reliable data transfer
- If we are less worried about speed, then we should be more worried about reliable transfer of data.
- We are going to want to keep track of state with a Finite State Machine (FSM).
- We want to abstract reliable services, the programmer shouldn't need to deal with the lower level aspects of things. 
	- We implement a reliable data transfer protocol for both the sender and receiver.
	- These go into a normal, unreliable channel.
	- It just looks like a direct reliable channel to the programmer.
- So if we want to know that something has been received, then we want to have the receiver *acknowledge* it.
- The complexity of reliable data transfer protocols will depend on characteristics of the unreliable channel.
- Getting started:
	- We will incrementally develop sender and receiver sides of reliable data transfer protocol (rdt) 
	- Consider only unidirectional data transfer
		- But control will flow in both directions
	- Use finite state machines (FSM) to specify sender and receiver.
- rdt 1:
	- Underlying channel is perfectly reliable, with no bit errors or loss of packets
	- Separate FSMs for sender and receiver:
		- Sender sends data into underlying channel
		- Receiver reads data from underlying channel
- rdt 2:
	- Underlying channel may flip bits in packet
		- Checksum to detect bit errors
	- How do we recover from errors? Acknowledgement!
	- ACK: the receiver explicitly tells the sender that the packet was received
	- Negative acknowledgement (NAK): receiver explicitly tells the sender that the packet had errors.
	- Stop and wait:
		- The sender must wait for the ACK/NAK before sending any more data.
	- FSM specifications:
		- The sender starts in wait for call. Once the call is received from the code, it sends a message.
		- When the message is sent, it goes to the wait for ACK or NAK state.
		- When one is received, we go back to the wait for call state.
		- The receiver only has one state. It just waits for data.
	- This has a fatal flaw:
		- We might never get an ACK. It could get lost. If ACK is lost, then we end up waiting forever.