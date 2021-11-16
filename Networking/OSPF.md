# OSPF
[Back to networking page](Networking.md)
- --
## What is OSPF?
Open Shortest Path First is a routing protocol for Internet Protocol networks. It uses a link state([Link state , distance vector & hybrid](Link%20state%20,%20distance%20vector%20&%20hybrid.md)) routing algorithm and falls into the group of interior gateway protocols, operating within a single autonomous system. It is defined as OSPF Version 2 in RFC 2328 for IPv4
- --
## Overview of OSPF Packet Types
|Packet Name|Type/Number|Function|
|:--:|:--:|:--|
|Hello|1|Discovers and maintains neighbors.|
|Database description|2|Summarizes database contents.|
|Link state request|3|Requests LSAs that need to be downloaded to requesting router. Only sent during Exchange, Loading, or Full state.|
|Link state update|4|Contains a list of the LSAs that are to be updated. Often used in flooding, as discussed later in this chapter.|
|Link state acknowledgment|5|Acknowledges the packets sent out during flooding to ensure efficient use of floods.|
### Source:
- [wiki](https://en.wikipedia.org/wiki/Open_Shortest_Path_First)
- [Youtube video](https://youtu.be/kfvJ8QVJscc)
- [Detailed YT video](https://youtu.be/k5z-H7PwLNk)
- [Packets type](https://www.ccexpert.us/ospf-network/types-of-ospf-packets.html)