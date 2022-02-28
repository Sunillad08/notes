# UDP
[Back to Networking page](./index.md)

---

## What is UDP?
**User Datagram Protocol**
UDP (User Datagram Protocol) is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.

---

## Why?
UDP uses a simple connectionless communication model with a minimum of protocol mechanisms. UDP provides checksums for data integrity, and port numbers for addressing different functions at the source and destination of the datagram. It has no handshaking dialogues, and thus exposes the user's program to any unreliability of the underlying network; there is no guarantee of delivery, ordering, or duplicate protection. If error-correction facilities are needed at the network interface level, an application may use Transmission Control Protocol [TCP](TCP.md) or Stream Control Transmission Protocol (SCTP) which are designed for this purpose.

UDP is suitable for purposes where error checking and correction are either not necessary or are performed in the application; UDP avoids the overhead of such processing in the protocol stack. Time-sensitive applications often use UDP because dropping packets is preferable to waiting for packets delayed due to retransmission, which may not be an option in a real-time system.

The protocol was designed by David P. Reed in 1980 and formally defined in RFC 768.

---

## UDP Header
![UDP header|700](https://i2.wp.com/ipwithease.com/wp-content/uploads/2018/01/091-udp-user-datagram-protocol-01.png)
A UDP datagram consists of a datagram header and a data section. The UDP datagram header consists of 4 fields, each of which is 2 bytes (16 bits). The data section follows the header and is the payload data carried for the application.

- Source port number
	This field identifies the sender's port, when used, and should be assumed to be the port to reply to if needed. If not used, it should be zero. If the source host is the client, the port number is likely to be an ephemeral port number. If the source host is the server, the port number is likely to be a well-known port number.
- Destination port number
	This field identifies the receiver's port and is required. Similar to source port number, if the client is the destination host then the port number will likely be an ephemeral port number and if the destination host is the server then the port number will likely be a well-known port number.
- Length
	This field specifies the length in bytes of the UDP header and UDP data. The minimum length is 8 bytes, the length of the header. The field size sets a theoretical limit of 65,535 bytes (8-byte header + 65,527 bytes of data) for a UDP datagram. However the actual limit for the data length, which is imposed by the underlying IPv4 protocol, is 65,507 bytes (65,535 bytes − 8-byte UDP header − 20-byte IP header).
	Using IPv6 jumbograms it is possible to have UDP datagrams of size greater than 65,535 bytes. RFC 2675 specifies that the length field is set to zero if the length of the UDP header plus UDP data is greater than 65,535.
- Checksum
	The checksum field may be used for error-checking of the header and data. This field is optional in IPv4, and mandatory in IPv6. The field carries all-zeros if unused.

---

### Sources
- [WIki](https://en.wikipedia.org/wiki/User_Datagram_Protocol)
- [Detailed UDP](https://youtu.be/HF_znV8x9a0)
- [TCP vs UDP](https://youtu.be/uwoD5YsGACg)