# Link state vs. distance vector vs. hybrid
[Back to networking page](Networking.md)
- --
## Link state
Each router floods information about itself (its link states) either to all other routers in the network or to a part of the network (area). Each router makes its own routing decision based on all received information and using the shortest path first (SPF) algorithm (also called the Dijkstra algorithm), which calculates the shortest path to any destination. Link-state protocols are fast to converge, have less routing traffic overhead, and scale well. However, because of their complexity, link-state protocols are more difficult to implement and maintain. The IP link-state protocols are [OSPF](OSPF.md) and Integrated IS-IS.

 ## Distance vector protocol
 In a distance vector protocol, routing decisions are made on a hop-by-hop basis. Each router relies on its neighbor routers to make the correct routing decisions. The router passes only the results of this decision (its routing table) to its neighbors. Distance vector protocols are typically slower to converge and do not scale well; however, they are easy to implement and maintain. Examples of distance vector protocols include [RIP](RIP.md) and Interior Gateway Routing Protocol (IGRP).
 
 ## Hybrid
 Routers running a hybrid protocol send changed information only when there is a change (similar to link-state protocols), but only to neighboring routers (similar to distance vector protocols).[EIGRP](EIGRP.md).
 - --
 ## Protocols 
|Category|Routing Protocol|
|:--|:--|
|Distance vector|RIPv1, RIPv2, IGRP|
|Link-state|OSPF, Integrated IS-IS|
|Hybrid|EIGRP|
 - --
 ### Source:
 - [website](https://www.ccexpert.us/network-design/distance-vector-versus-linkstate-versus-hybrid-protocols.html)