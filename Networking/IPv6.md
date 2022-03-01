# IPv6
[Back to networking page](./index.md)

---

## What is IPv6?
An IPv6 packet is the smallest message entity exchanged using Internet Protocol [IP](IP.md)version 6 (IPv6). 128 bits length and developed by IETF IPv6 was invented because [IPv4](IPv4.md) IP's are limited.

---

## IPv6 format
IPv6 format : XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX

Length of IPv6 address is 128 bits
Each octet can have values 0000 -> FFFF 
Length of octet is 16 bits.
Example:
2001:db8:3333:4444:5555:6666:7777:8888. 2001:db8:3333:4444:CCCC:DDDD:EEEE:FFFF.

![ip format](https://www.redhat.com/sysadmin/sites/default/files/styles/embed_medium/public/2019-09/IPv6%20addresses.png?itok=AlrTREni)

---

## IPv6 Header
![header](https://upload.wikimedia.org/wikipedia/commons/6/6b/IPv6_header_rv1.png)

- Version (4 bits)
	The constant 6 (bit sequence 0110).
- Traffic Class (6+2 bits)
	The bits of this field hold two values. The six most-significant bits hold the differentiated services field (DS field), which is used to classify packets. Currently, all standard DS fields end with a '0' bit. Any DS field that ends with two '1' bits is intended for local or experimental use.
	The remaining two bits are used for Explicit Congestion Notification (ECN); priority values subdivide into ranges: traffic where the source provides congestion control and non-congestion control traffic.
- Flow Label (20 bits)
	A high-entropy identifier of a flow of packets between a source and destination. A flow is a group of packets, e.g., a TCP session or a media stream. The special flow label 0 means the packet does not belong to any flow (using this scheme). An older scheme identifies flow by source address and port, destination address and port, protocol (value of the last Next Header field). It has further been suggested that the flow label be used to help detect spoofed packets.
- Payload Length (16 bits)
	The size of the payload in octets, including any extension headers. The length is set to zero when a Hop-by-Hop extension header carries a Jumbo Payload option.
- Next Header (8 bits)
	Specifies the type of the next header. This field usually specifies the transport layer protocol used by a packet's payload. When extension headers are present in the packet this field indicates which extension header follows. The values are shared with those used for the IPv4 protocol field, as both fields have the same function (see List of IP protocol numbers).
- Hop Limit (8 bits)
	Replaces the time to live field in IPv4. This value is decremented by one at each forwarding node and the packet is discarded if it becomes 0. However, the destination node should process the packet normally even if received with a hop limit of 0.
- Source Address (128 bits)
	The unicast IPv6 address of the sending node.
- Destination Address (128 bits)
	The IPv6 unicast or multicast address of the destination node(s).


In order to increase performance, and since current link layer technology and transport layer protocols are assumed to provide sufficient error detection, the header has no checksum to protect it.

---

## Extension headers
![extension headers](https://media.geeksforgeeks.org/wp-content/uploads/next-header-2.png)

---

**Difference between IPv4 and IPv6**

![difference](https://4.bp.blogspot.com/-pBo1LxiPYoE/WNOgKMJmBII/AAAAAAAAAeY/D_kfnwJQYIAc74IFyxcjgQJ489ZsFtf-gCLcB/s1600/p4.png)

---

### Source
- [Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet)
- [Youtube 1](https://youtu.be/1GbJUAcHfKU)
- [Headers YouTube ](https://youtu.be/ukEJ3V7iX94)
- [Difference Youtube](https://youtu.be/MYYaeu_qiH4)
- [IBM](https://www.ibm.com/docs/en/ts4500-tape-library?topic=functionality-ipv4-ipv6-address-formats)