# IP address
[Back to networking page](../index.md)
- --
## What is IP address?
Internet Protocol address
Logical addressing with numerical values
IP gives you access to Internet and unique number so others can identify you.
- --
## Why IP ?
On internet we need to communicate using packets . So where should we send one? That's why to identify you as one on billions computers we need IP. Also Internet Protocol addressing gives to access to internet
- --
## How do we get one?
We get IP address based on router , subnetting and many more things.
[DHCP](DHCP.md) protocol gives us IP address.
In home network router is your DHCP server.
- --
## Private & Public IP?
Public IP is IP which is displayed to all other devices on Internet but as IPv4 is limited so some devices share same public IP.
Private IP is IP given in Internal network and using [Subnetting](Subnetting.md) we can get many devices to share same public IP.
- -- 
## IP addresses divided in classes: 
 ![ip address blocks|700](https://4.bp.blogspot.com/--yi2nvFpat4/U-3d8GB9KvI/AAAAAAAANoo/EjfJIHi8jM4/s1600/Classes%2Bof%2BIP.png)
 
  ![ip address blocks|700](https://embeddedgeeks.com/wp-content/uploads/2020/06/ip_Class-1.png)
- --
## Class types
### Classfull addressing
Classful Routing does not import subnet mask. And in this also subnet mask is provided after the route update. In classful routing, subnet mask is same throughout, does not vary for all devices.

### Classless addressing
Classless Routing imports subnet mask and in this, triggered updates are used. In classless routing, VLMS (Variable Length Subnet Mask) is supported and also CIDR (Classless Inter-Domain Routing).

![classless vs classfull|700](https://i1.wp.com/ipwithease.com/wp-content/uploads/2018/01/119-classful-vs-classless-routing-01.png?resize=686%2C568)
- --
## Two types of IP address styles:
 - Dynamic IP address
	 - IP changes when reconnected
 - Static IP address
	 - IP will be same every time

- --
 ## Two types of IP address
 - [IPv4](IPv4.md)
	 - 0-255 count
	 - xxx.xxx.xxx.xxx format
	 - 32 bit address
	 - 2^32 Devices can be addressed
- [IPv6](IPv6.md)
	- Running out of IP address hence IPv6
	- 128 bits address
	- XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX:XXXX
	- 2^128 devices can be connected

![headers|700](https://www.researchgate.net/profile/Muzhir-Al-Ani/publication/269810379/figure/fig1/AS:295073662160901@1447362451826/Comparison-of-IPv4-and-IPv6-headers-structures-15.png)

**Difference between IPv4 and IPv6**

![difference|700](https://4.bp.blogspot.com/-pBo1LxiPYoE/WNOgKMJmBII/AAAAAAAAAeY/D_kfnwJQYIAc74IFyxcjgQJ489ZsFtf-gCLcB/s1600/p4.png)
- --
### Sources :
- [Youtube](https://www.youtube.com/watch?v=8npT9AALbrI&list=WL&index=97&ab_channel=TechTerms)
- [Techquickie](https://www.youtube.com/watch?v=aor29pGhlFE&ab_channel=Techquickie)
- [Youtube](https://youtu.be/HKM7qwP5Uj0)
- [Classfull vs Classless](https://www.geeksforgeeks.org/difference-between-classful-routing-and-classless-routing/)