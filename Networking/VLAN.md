# VLAN
[Bacl to networking page](index.md)
- --
## What is VLAN?
**Virtual LAN (VLAN)** is a concept in which we can divide the devices logically on layer 2 (data link layer). Generally, layer 3 devices divide broadcast domain but broadcast domain can be divided by switches using the concept of VLAN.

A virtual local area network is a logical subnetwork that groups a collection of devices from different physical LANs. Large business computer networks often set up VLANs to re-partition a network for improved traffic management. Several kinds of physical networks support virtual LANs, including Ethernet and Wi-Fi.
- --
## Why?
When set up correctly, virtual LANs improve the performance of busy networks. VLANs can group client devices that communicate frequently with each other. The traffic among devices split across two or more physical networks is usually handled by a network's core routers. With a VLAN, that traffic is handled more efficiently by network switches.

VLAN ranges :
VLAN 0, 4095: These are reserved VLAN which cannot be seen or used.
VLAN 1: It is the default VLAN of switches. By default, all switch ports are in VLAN. This VLAN can’t be deleted or edit but can be used.
VLAN 2-1001: This is a normal VLAN range. We can create, edit and delete these VLAN.
VLAN 1002-1005: These are CISCO defaults for fddi and token rings. These VLAN can’t be deleted.
Vlan 1006-4094: This is the extended range of Vlan.

![vlan|700](https://cyberhoot.com/wp-content/uploads/2020/01/Image12005.gif)
- --
## 802.1q
IEEE 802.1Q, often referred to as Dot1q, is the networking standard that supports virtual LANs (VLANs) on an IEEE 802.3 Ethernet network. The standard defines a system of VLAN tagging for Ethernet frames and the accompanying procedures to be used by bridges and switches in handling such frames. The standard also contains provisions for a quality-of-service prioritization scheme commonly known as IEEE 802.1p and defines the Generic Attribute Registration Protocol.

![802.1q|900](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0e/Ethernet_802.1Q_Insert.svg/1328px-Ethernet_802.1Q_Insert.svg.png)
- --
### Source:
- [Youtube video](https://youtu.be/jC6MJTh9fRE)
- [Certbros](https://youtu.be/A9lMH0ye1HU)
- [Neso academy](https://youtu.be/ez24W5oTU3U)
- [Website](https://www.lifewire.com/virtual-local-area-network-817357)
- [geeksforgeeks](https://www.geeksforgeeks.org/virtual-lan-vlan/)
- [Wikipedia](https://en.wikipedia.org/wiki/Virtual_LAN)
- [wikipedia 802.1q](https://en.wikipedia.org/wiki/IEEE_802.1Q)