# Packets
[Back to Networking page](./index.md)

---

## What is packet?
 Packet is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data the latter is also known as the payload. Control information provides data for delivering the payload (e.g., source and destination network addresses, error detection codes, or sequencing information). Typically, control information is found in packet headers and trailers.

---

## Why we use packet?
Packet is PDU(Protocol Data Unit) in Network layer.
Packet headers are attached to outgoing data. Packets can pass through many gateways before reaching their destinations.  At the destination network, the headers are stripped from the packets and the data is sent to the appropriate host.

---

## Packet Headers
Different headers for different format
![diagram of IPv4|700](https://erg.abdn.ac.uk/users/gorry/course/images/ip-header.gif)

Check more about IP header [Two types of IP address](IP.md#Two%20types%20of%20IP%20address)

---

### Source
- [Wiki](https://en.wikipedia.org/wiki/Network_packet)