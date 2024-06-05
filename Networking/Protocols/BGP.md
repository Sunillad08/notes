# BGP
[Back to networking page](../index.md)

---

## What is BGP?
Border Gateway Protocol (BGP) is a standardized exterior gateway protocol designed to exchange routing and reachability information among autonomous systems (AS) on the Internet. BGP is classified as a path-vector routing protocol and it makes routing decisions based on paths, network policies, or rule-sets configured by a network administrator.

BGP used for routing within an autonomous system is called Interior Border Gateway Protocol, Internal BGP (iBGP). In contrast, the Internet application of the protocol is called Exterior Border Gateway Protocol, External BGP (eBGP).

![BGP](https://www.ajsnetworking.com/wp-content/uploads/2018/01/Overview-Topo.png)

Point to point communication.

---

## Working of BGP
BGP neighbors, called peers, are established by manual configuration among routers to create a TCP session on [Ports](Ports.md) 179. A BGP speaker sends 19-byte keep-alive messages every 30 seconds (protocol default value, tunable) to maintain the connection. Among routing protocols, BGP is unique in using TCP as its transport protocol.

---

## Header of BGP
![header of BGP](https://image1.slideserve.com/3012582/bgp-messages-l.jpg)

---

## BGP Messages
|Message|Purpose|
|:--|:--|
|OPEN |Sets up and establishes BGP adjacency|
|UPDATE|Advertises, updates, or withdraws routes|
|NOTIFICATION|Indicates an error condition to a BGP neighbor|
|KEEPALIVE|Ensures that BGP neighbors are still alive|

---

### Source:
- [Wikipedia](https://en.wikipedia.org/wiki/Border_Gateway_Protocol)
- [Bitten tech YT](https://youtu.be/nePkGSCuhTU)
- [Cisco](https://www.ciscopress.com/articles/article.asp?p=2756480&seqNum=3)