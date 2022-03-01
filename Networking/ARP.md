# ARP
[Back to networking page](./index.md)

---

## What is ARP?
**Address Resolution Protocol**
The Address Resolution Protocol(ARP) is a communication protocol used to discover the data-link layer address(Layer 2 address like Media Access Control ie [MAC](MAC.md) associated with an Internet layer address(Layer 3 address like [IP](IP.md). ... As a result, ARP is said to be a link layer protocol.

---

## Why?
Devices in a Local Area Network(LAN) are programmed to communicate using link layer addresses. Switches are not configured for a standard that will allow destination decisions to be based on IP within the same broadcast domain. A device that is not connected to the internet will not have an IP address. In that case, the network has to resort to using MAC addresses for communication. If a device wants to communicate with another device in the same LAN, it needs to know the MAC address of the other device’s network interface. This allows for the communication between the two end devices to be unicast.

---

## How does it work?
- Every device that is capable of handling IPv4 packets has an ARP table. An ARP table consists of IPv4 address to MAC address mappings. Switches do not have an ARP table as they are not equipped to handle IP packets. However, switches maintain another kind of cache mapping the MAC address of the non-switch devices connected to this LAN to the port where packets should go to reach that device. Switches will send out the packet on all the enabled ports if they do not have the destination MAC address in the cache.

![ARP](https://www.section.io/engineering-education/address-resolution-protocol/arpExample.jpg)
- When device 1 with IP 192.168.10.154 wants to send a packet to device 3 with IP 192.168.10.160, it looks into its ARP cache to fetch device 3’s MAC address. If the IP to MAC translation for device 3 does not exist in the ARP cache, device 1 sends a broadcast packet to the network using the ARP protocol to ask “who has 192.168.10.160?".
- All the devices in that network receive the ARP broadcast packet. The device with the requested IP address will reply with an ARP response that contains its MAC address. Note that the ARP response is unicast i.e it is sent only to the device that sent the ARP request. On receiving the ARP response, device 1 updates its ARP table with an entry for device 3. The switch too, updates its ARP cache noting which of its ports is connected to device 3.

_On Linux systems, ARP table can be displayed with the command “arp -an”._
_On Windows systems, ARP table can be displayed with the command “arp -a”._

---

### Sources
- [website](https://www.section.io/engineering-education/address-resolution-protocol/)
- [Youtube 1](https://youtu.be/tXzKjtMHgWI)
- [Youtube 2](https://youtu.be/cn8Zxh9bPio)
- [Youtube 3](https://youtu.be/EC1slXCT3bg)