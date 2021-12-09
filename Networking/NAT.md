# NAT : Network Address Translation
[Back to Networking page](Networking.md)
- --
## What is NAT?
NAT stands for network address translation. It’s a way to map multiple local private addresses to a public one before transferring the information. Organizations that want multiple devices to employ a single IP address use NAT, as do most home routers.
- --
## Why we need NAT?
- IP addresses identify each device connected to the internet. The existing IP version 4 (IPv4) uses 32-bit numbered IP addresses, which allows for 4 billion possible IP addresses, which seemed like more than enough when it launched in the 1970s.

- However, the internet has exploded, and while not all 7 billion people on the planet access the internet regularly, those that do often have multiple connected devices: phones, personal desktop, work laptop, tablet, TV, even refrigerators.

- Therefore, the number of devices accessing the internet far surpasses the number of IP addresses available. Routing all of these devices via one connection using NAT helps to consolidate multiple private IP addresses into one public IP address. This helps to keep more public IP addresses available even while private IP addresses proliferate.

![NAT](https://i0.wp.com/networkustad.com/wp-content/uploads/2019/10/Dynamic-NAT-Configration.png)
- --
## Types of NAT (CompTIA)
1. Static NAT - **SNAT**
When the local address is converted to a public one, this NAT chooses the same one. This means there will be a consistent public IP address associated with that router or NAT device.

2. Dynamic NAT - **DNAT**
Instead of choosing the same IP address every time, this NAT goes through a pool of public IP addresses. This results in the router or NAT device getting a different address each time the router translates the local address to a public address.

3. PAT - **PAT**
PAT stands for port address translation. It’s a type of dynamic NAT, but it bands several local IP addresses to a singular public one. Organizations that want all their employees’ activity to use a singular IP address use a PAT, often under the supervision of a network administrator.

- --
### Sources 
- [Computerphile](https://youtu.be/01ajHxPLxAw)
- [CompTIA page](https://www.comptia.org/content/guides/what-is-network-address-translation)
- [Youtube](https://youtu.be/FTUV0t6JaDA)
- [Youtube](https://youtu.be/47PUj7OSGkA)
- [NAT woking](https://youtu.be/qij5qpHcbBk)
- [SNAT,DNAT,PAT](https://youtu.be/wg8Hosr20yw)