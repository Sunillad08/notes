# RIP
[Back to networking page](../index.md)
- --
## What is RIP?
The **Routing Information Protocol** (RIP) is one of the oldest distance-vector routing protocols which employs the hop count as a routing metric. RIP prevents routing loops by implementing a limit on the number of hops allowed in a path from source to destination. The largest number of hops allowed for RIP is 15, which limits the size of networks that RIP can support.
- --
## RIP timers 
- **Update timer**: The default timing for routing information being exchanged by the routers operating RIP is 30 seconds. Using an Update timer, the routers exchange their routing table periodically.
- **Invalid timer**: If no update comes until 180 seconds, then the destination router considers it invalid. In this scenario, the destination router mark hop counts as 16 for that router.
- **Hold down timer**: This is the time for which the router waits for neighbour router to respond. If the router isn’t able to respond within a given time then it is declared dead. It is 180 seconds by default.
- **Flush time**: It is the time after which the entry of the route will be flushed if it doesn’t respond within the flush time. It is 60 seconds by default. This timer starts after the route has been declared invalid and after 60 seconds i.e time will be 180 + 60 = 240 seconds.

- --
### Source:
- [Wiki](https://en.wikipedia.org/wiki/Routing_Information_Protocol)
- [geeksforgeeks](https://www.geeksforgeeks.org/routing-information-protocol-rip/)
- [Youtube video](https://youtu.be/rIU2dKnPd0E)
- [Youtube detailed](https://youtu.be/pQQ5wNgbQw8)