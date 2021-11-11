# EIGRP
[Networking](Networking.md)
- --
## What is EIGRP?
Enhanced Interior Gateway Routing Protocol (EIGRP) is a network protocol that enables routers to exchange information more efficiently than earlier network protocols, such as Interior Gateway Routing Protocol (IGRP) or Border Gateway Protocol (BGP).
- --
To pass messages and facilitate session management, EIGRP uses five package types:

- **HELLO** packets : Sent out at regular intervals to facilitate the neighbor discovery process.
- **QUERY** packets : Used by a router to advertise that a route is in an active state and to request alternate path information from neighbors.
- **REPLY** packets : Sent after an entire QUERY packet has been received to acknowledge that packet's receipt.
- **REQUEST** packets : Used to request specific information from one or more neighbors, similar to QUERY packets but sent unreliably -- no notification if delivery fails.
- **UPDATE** packets : Convey information about destinations and their reachability.
- --
### Source:
- [cisco](https://www.cisco.com/c/en/us/support/docs/ip/enhanced-interior-gateway-routing-protocol-eigrp/16406-eigrp-toc.html)
- [Youtube](https://youtu.be/QyymlFWDEgM)