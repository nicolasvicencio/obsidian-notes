- TCP, or Transmission Control Protocol, is one of the main protocols operating at the Transport Layer ( Layer 4) of [[OSI model]]

- It is a connection-oriented, reliable protocol that provides a dependable and ordered delivery of data between two devices over a network

- TCP ensures that data sent from one application on a device is received accurately and in the correct order by another application on a different device

## Characteristics

- **Connection oriented**: Establishes a connection between the sender and receiver before any data is exchanged, This connection is a virtual circuit that ensure reliable and ordered data transfer.
- **Reliability**: TCP guarantees reliable delivery of data. It achieves this through mechanisms such as acknowledgments (ACK) and re transmission of lost or corrupted packets, if a segment of data is not acknowledged, TCP automatically resends the segment
- **Ordered Data Transfer**: TCP ensure that data is delivered int the correct order. if segments of data arrive out of order. TCP reorders then before passing them to the higher-layer application

## TCP 3-Way Handshake

- The TCP Three-way handshake is a process used to establish a reliable connection between two devices before they begin data transmission.
- It involves a series of three messages exchanged between the sender ( client) and the receiver (server )

![[Pasted image 20231221104550.png]]

#### Steps

- **SYN** (Synchronize): The process begins with the client sending a TCP segment with the SYN ( Synchronize) flag set. This initial message indicates the client's intention to establish a connection and include an initial sequence number (ISN), which is a randomly chosen value.
- **SYN-ACK** (Synchronize-Acknowledge): Upon receiving the SYN segment, the server responds with a TCP segment that has both the SYN and ACK flags set, The acknowledgment (ACK) number is set to one more than the initial sequence number receive in the client's SYN segment. The sever also general its own initial sequence number
- **ACK**: Finally the client acknowledges the server's response by sending a TCP segment with the ACK flag set. The acknowledgment number is set to one more than the server's initial sequence number
- After the three-way handshake is complete, the devices can exchange data int both directions. The acknowledgement numbers in subsequent segments are used to confirm the receipt of data and to manage the flow of information.

### Ports

- TCP uses port numbers to distinguish between different services or applications on a device
- The maximum port number in the TCP/IP protocol suite is 65.535
