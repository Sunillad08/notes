# Network topologies
[Back to Networking page](./index.md)

---

## Bus topology

- Nodes are directly connected to common linear or branched half duplex link called bus.
- Passive topology
- Requires proper termination at both ends to avoid reflection

**Advantages  :**
- Easy to install 
- Used in small networks
- Less cabling cost
- Easy to expand

**Disadvantages  :**
- Can't handle heavy traffic
- BNC connectors used for expansion attenuates signal
- Improper termination can reflect signal

![Bus](https://www.dnsstuff.com/wp-content/uploads/2019/09/Bus-Topology.jpg)

---

## Ring topology

- Each nodes connect to exactly two other nodes
- Active network 
- Message flows around ring in one direction
- No termination as there is no end to ring
- Token passing : it allows station to transmit when it holds token
- Sequential manner transmission
- Each node has to recreate packet

**Advantages :**
- Equal access to token
- No standing waves produced

**Disadvantages :**
- Failure of one node can affect whole network
- Difficult to troubleshoot
- Adding and removing computers disturbs network activity

![Ring](https://www.dnsstuff.com/wp-content/uploads/2019/09/Ring-Topology.jpg)

---

## Star topology

 - All nodes are connected to central hub or switch
 - No direct communication among computers
 - Concentrated network
 - Hub send packets to destination 
 - Active or passive depend on central hub

**Advantages :**
- More devices can be connected in large distance
- Isolated network due to central hub management
- High reliability
- Easy to expand

**Disadvantages :**
- If central hub fails then network is down
- High cabling cost

![Star](https://www.dnsstuff.com/wp-content/uploads/2019/09/Star-Topology.jpg)

---

## Mesh topology

- Every node connected to every other node
- Dedicated link
- n(n-1)/2 physical cables are required
- Passive network

**Advantages :**
- High reliability
- Data security because of dedicated link
- Easy to troubleshoot

**Disadvantages :**
- High cabling cost
- Expensive
- Installation and configuration is difficult

![mesh](https://www.dnsstuff.com/wp-content/uploads/2019/08/what-is-mesh-topology-1024x536.png)

---

## Tree topology

- Arranged like branches of tree
- Variation of star topology
- Central hub is connected to many other hubs
- Parent child topology
- Active network

**Advantages :**
- Large distance covered
- Allows network to isolate 
- Signal can go for long distance

**Disadvantages :**
- Failure of central hub breaks down
- Cabling cost is more

![tree](https://www.dnsstuff.com/wp-content/uploads/2019/09/Tree-Topology.jpg)

---

## Hybrid topology

Mixture of all topologies like bus and ring

![hybrid](https://www.dnsstuff.com/wp-content/uploads/2019/09/Hybrid-Topology.jpg)

---

### Sources :
- [website](https://www.dnsstuff.com/what-is-network-topology)
- [Youtube](https://youtu.be/e0CWszGpgAE)