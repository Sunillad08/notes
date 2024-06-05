# TCP
[Back to Networking page](../index.md)

---

## What is TCP
**Transmission Control Protocol**

The **Transmission Control Protocol** (TCP) is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the Internet Protocol (IP). Therefore, the entire suite is commonly referred to as TCP/IP. TCP provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network. Major internet applications such as the World Wide Web, email, remote administration, and file transfer rely on TCP, which is part of the Transport Layer of the TCP/IP suite. SSL/TLS often runs on top of TCP.

---

## Why TCP?
TCP is connection-oriented, and a connection between client and server is established before data can be sent. The server must be listening (passive open) for connection requests from clients before a connection is established. Three-way handshake (active open), retransmission, and error-detection adds to reliability but lengthens latency. Applications that do not require reliable data stream service may use the User Datagram Protocol [UDP](Protocols/UDP.md), which provides a connectionless datagram service that prioritizes time over reliability. TCP employs network congestion avoidance. However, there are vulnerabilities to TCP including denial of service, connection hijacking, TCP veto, and reset attack.

---

## TCP Header

![TCP](https://www.gatevidyalay.com/wp-content/uploads/2018/09/TCP-Header-Format.png)

- Source port (16 bits) : Identifies the sending port.
- Destination port (16 bits) : Identifies the receiving port.
- Sequence number (32 bits) : Has a dual role:
	If the SYN flag is set (1), then this is the initial sequence number. The sequence number of the actual first data byte and the acknowledged number in the corresponding ACK are then this sequence number plus 1.
	If the SYN flag is clear (0), then this is the accumulated sequence number of the first data byte of this segment for the current session.
- Acknowledgment number (32 bits) : If the ACK flag is set then the value of this field is the next sequence number that the sender of the ACK is expecting. This acknowledges receipt of all prior bytes (if any). The first ACK sent by each end acknowledges the other end's initial sequence number itself, but no data.
- Data offset (4 bits) : Specifies the size of the TCP header in 32-bit words. The minimum size header is 5 words and the maximum is 15 words thus giving the minimum size of 20 bytes and maximum of 60 bytes, allowing for up to 40 bytes of options in the header. This field gets its name from the fact that it is also the offset from the start of the TCP segment to the actual data.
- Reserved (3 bits) : For future use and should be set to zero.
- Flags (9 bits) : Contains 9 1-bit flags (control bits) as follows:
	- NS (1 bit): ECN-nonce - concealment protection
	- CWR (1 bit): Congestion window reduced (CWR) flag is set by the sending host 				   to indicate that it received a TCP segment with the ECE flag set and had 	         responded in congestion control mechanism.
	- ECE (1 bit): ECN-Echo has a dual role, depending on the value of the SYN flag. It indicates:
	  	If the SYN flag is set (1), that the TCP peer is ECN capable.
		If the SYN flag is clear (0), that a packet with Congestion Experienced flag set (ECN=11) in the IP header was received during normal transmission. This serves as an indication of network congestion (or impending congestion) to the TCP sender.
	- URG (1 bit): Indicates that the Urgent pointer field is significant
	- ACK (1 bit): Indicates that the Acknowledgment field is significant. All packets after the initial SYN packet sent by the client should have this flag set.
	- PSH (1 bit): Push function. Asks to push the buffered data to the receiving application.
	- RST (1 bit): Reset the connection
	- SYN (1 bit): Synchronize sequence numbers. Only the first packet sent from each end should have this flag set. Some other flags and fields change meaning based on this flag, and some are only valid when it is set, and others when it is clear.
	- FIN (1 bit): Last packet from sender
- Window size (16 bits) : The size of the receive window, which specifies the number of window size units that the sender of this segment is currently willing to receive. (See § Flow control and § Window scaling.)
- Checksum (16 bits) : The 16-bit checksum field is used for error-checking of the TCP header, the payload and an IP pseudo-header. The pseudo-header consists of the source IP address, the destination IP address, the protocol number for the TCP protocol (6) and the length of the TCP headers and payload (in bytes).
- Urgent pointer (16 bits) : If the URG flag is set, then this 16-bit field is an offset from the sequence number indicating the last urgent data byte.
- Options (Variable 0–320 bits, in units of 32 bits)
	The length of this field is determined by the data offset field. Options have up to three fields: Option-Kind (1 byte), Option-Length (1 byte), Option-Data (variable). The Option-Kind field indicates the type of option and is the only field that is not optional. Depending on Option-Kind value, the next two fields may be set. Option-Length indicates the total length of the option, and Option-Data contains data associated with the option, if applicable. For example, an Option-Kind byte of 1 indicates that this is a no operation option used only for padding, and does not have an Option-Length or Option-Data fields following it. An Option-Kind byte of 0 marks the end Of options, and is also only one byte. An Option-Kind byte of 2 is used to indicate Maximum Segment Size option, and will be followed by an Option-Length byte specifying the length of the MSS field. Option-Length is the total length of the given options field, including Option-Kind and Option-Length fields. So while the MSS value is typically expressed in two bytes, Option-Length will be 4. As an example, an MSS option field with a value of 0x05B4 is coded as (0x02 0x04 0x05B4) in the TCP options section.

---

## TCP Connection
Check [TCP_IP_3_way_handshake](TCP_IP_3_way_handshake.md) for connection info

For termination this is procedure
![TCP close connection](http://www.cablefree.net/support/radio/software/images/f/fc/Image2001.gif)

---

### Sources
- [wikipedia](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)
- [TCP connection](https://youtu.be/zlIHLnOigmA)
- [Detailed TCP 1](https://youtu.be/c8aet11HNxg)
- [Detailed TCP 2](https://youtu.be/hsNuqtfxgRI)
- [TCP Vs UDP](https://youtu.be/cA9ZJdqzOoU)