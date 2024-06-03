# IPv4
[Back to networking page](./index.md)

---

## What is IPv4?
Check what is [IP](IP.md)
Internet Protocol version 4 (IPv4) is the fourth version of the Internet Protocol (IP). It is one of the core protocols of standards-based internetworking methods in the Internet and other packet-switched networks. IPv4 was the first version deployed for production on SATNET in 1982 and on the ARPANET in January 1983. It is still used to route most Internet traffic today, despite the ongoing deployment of a successor protocol, [IPv6](IPv6.md).

-- -

## IPv4 format
- Format xxx:xxx:xxx:xxx
- Length of IPv4 address is 32 bits.
- Length of each octet is 8bits
- Octet can have value from 00 -> FF

Example:
191.52.148.36
192.168.0.104

-- -

## Header format
![header](https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/IPv4_Packet-en.svg/1200px-IPv4_Packet-en.svg.png)

![header](https://media.geeksforgeeks.org/wp-content/uploads/20230512140024/Screenshot-(359).png)

- **Version** :
	The first header field in an IP packet is the four-bit version field. For IPv4, this is always equal to 4.
- **Internet Header Length (IHL)** :
	The IPv4 header is variable in size due to the optional 14th field (options). The IHL field contains the size of the IPv4 header, it has 4 bits that specify the number of 32-bit words in the header. The minimum value for this field is 5,which indicates a length of 5 × 32 bits = 160 bits = 20 bytes. As a 4-bit field, the maximum value is 15, this means that the maximum size of the IPv4 header is 15 × 32 bits = 480 bits = 60 bytes.
- **Type of service / Differentiated Services Code Point (DSCP)** :
	Originally defined as the type of service (ToS), this field specifies differentiated services (DiffServ) per RFC 2474. Real-time data streaming makes use of the DSCP field. An example is Voice over IP (VoIP), which is used for interactive voice services.
- **Total Length** :
	This 16-bit field defines the entire packet size in bytes, including header and data. The minimum size is 20 bytes (header without data) and the maximum is 65,535 bytes. All hosts are required to be able to reassemble datagrams of size up to 576 bytes, but most modern hosts handle much larger packets. Links may impose further restrictions on the packet size, in which case datagrams must be fragmented. Fragmentation in IPv4 is performed in either the sending host or in routers. Reassembly is performed at the receiving host.
- **Identification** :
	This field is an identification field and is primarily used for uniquely identifying the group of fragments of a single IP datagram. Some experimental work has suggested using the ID field for other purposes, such as for adding packet-tracing information to help trace datagrams with spoofed source addresses, but RFC 6864 now prohibits any such use.
- **Flags** :
	A three-bit field follows and is used to control or identify fragments. They are (in order, from most significant to least significant):
	bit 0: Reserved; must be zero.
	bit 1: Don't Fragment (DF)
	bit 2: More Fragments (MF)
	If the DF flag is set, and fragmentation is required to route the packet, then the packet is dropped. This can be used when sending packets to a host that does not have resources to perform reassembly of fragments. It can also be used for path MTU discovery, either automatically by the host IP software, or manually using diagnostic tools such as ping or traceroute.
	For unfragmented packets, the MF flag is cleared. For fragmented packets, all fragments except the last have the MF flag set. The last fragment has a non-zero Fragment Offset field, differentiating it from an unfragmented packet.
- **Fragment offset** :
	This field specifies the offset of a particular fragment relative to the beginning of the original unfragmented IP datagram in units of eight-byte blocks. The first fragment has an offset of zero. The 13 bit field allows a maximum offset of (213 – 1) × 8 = 65,528 bytes, which, with the header length included (65,528 + 20 = 65,548 bytes), supports fragmentation of packets exceeding the maximum IP length of 65,535 bytes.
- **Time to live (TTL)** :
	An eight-bit time to live field limits a datagram's lifetime to prevent network failure in the event of a routing loop. It is specified in seconds, but time intervals less than 1 second are rounded up to 1. In practice, the field is used as a hop count—when the datagram arrives at a router, the router decrements the TTL field by one. When the TTL field hits zero, the router discards the packet and typically sends an ICMP time exceeded message to the sender.
	The program traceroute sends messages with adjusted TTL values and uses these ICMP time exceeded messages to identify the routers traversed by packets from the source to the destination.
- **Protocol** :
	This field defines the protocol used in the data portion of the IP datagram. IANA maintains a list of IP protocol numbers as directed by RFC 790.
- **Header checksum** ::
	The 16-bit IPv4 header checksum field is used for error-checking of the header. When a packet arrives at a router, the router calculates the checksum of the header and compares it to the checksum field. If the values do not match, the router discards the packet. Errors in the data field must be handled by the encapsulated protocol. Both UDP and TCP have separate checksums that apply to their data.
	When a packet arrives at a router, the router decreases the TTL field in the header. Consequently, the router must calculate a new header checksum.
- **Source address** :
	This field is the IPv4 address of the sender of the packet. Note that this address may be changed in transit by a network address translation device.
- **Destination address** :
	This field is the IPv4 address of the receiver of the packet. As with the source address, this may be changed in transit by a network address translation device.
	

---

## Difference between IPv4 and IPv6

![difference](https://4.bp.blogspot.com/-pBo1LxiPYoE/WNOgKMJmBII/AAAAAAAAAeY/D_kfnwJQYIAc74IFyxcjgQJ489ZsFtf-gCLcB/s1600/p4.png)

---

### Source
- [wiki](https://en.wikipedia.org/wiki/IPv4)
- [Detailed Youtube Video](https://youtu.be/zt95uE42gIs)
- [IBM](https://www.ibm.com/docs/en/ts4500-tape-library?topic=functionality-ipv4-ipv6-address-formats)
- [Differnce Youtube](https://youtu.be/MYYaeu_qiH4)