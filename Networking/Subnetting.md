# Subnetting
[Back to Networking page](Networking.md)
- --
## What is subnetting?
A subnetwork or subnet is a logical subdivision of an IP network. The practice of dividing a network into two or more networks is called subnetting. Computers that belong to the same subnet are addressed with an identical most-significant bit-group in their IP addresses. 

Logical subdivision of a network is called subnetting.
- --
## Why subnetting required?
- Security
- Similar IP address format
- saving IPv4 IP's
- organizing network
- Reduce congestion
- --
## How to do subnetting?
*Many methods are there but we are going to see only CIDR*
a.b.c.d / x is CIDR format (Classless inter domain routing)
where a,b,c,d are octets and x is value that denotes common bits from left to right
example : 192.168.0.1/24 -> 255 Devices can be identified
Check [IP](IP.md) for classes about subnetting in IP's classes.

![wiki|700](https://upload.wikimedia.org/wikipedia/commons/b/b3/Subnetting_Concept.svg)

![subnetting|700](https://miro.medium.com/max/1400/0*xvktLgjkeydPSp5M.png)
- --
## Common terms in subnetting
**Broadcast ID/address**
An address that enables transmission to every node in a local network. The address is the highest numeric value of the address format being used. An Ethernet broadcast address is all binary 1's. An IP broadcast address is the highest number in its class.The Ethernet **broadcast address** is distinguished by having all of its bits set to 1. As such, its MAC address is the hexadecimal value of FF:FF:FF:FF:FF:FF. The broadcast address is used by multiple protocols such as ARP, the Routing Information Protocol (RIP), and other protocols that must transmit data before they know the local subnet mask.

**Network ID** is the portion of an IP address that identifies the TCP/IP network on which a host resides. The network ID portion of an IP address uniquely identifies the host's network on an internetwork, while the host ID portion of the IP address identifies the host within its network.

**Host Range**
Number of host that can connect to network is host range.
Host range is always available IP - 2 .
- --
### Sources
- [Wikipedia](https://en.wikipedia.org/wiki/Subnetwork)
- [Youtube](https://youtu.be/OqsXzkXfwRw)
- [subnetting YT](https://www.youtube.com/watch?v=ecCuyq-Wprc)
- [Network id and broadcast id](https://www.youtube.com/watch?v=uHabBNAFakA)