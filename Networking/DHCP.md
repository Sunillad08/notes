# DHCP 
[Back to networking page](./index.md)

---

## What is DHCP?
Dynamic Host Configuration Protocol is protocols that assign [IP](IP.md) to connected devices.
The **Dynamic Host Configuration Protocol** is a network management protocol used on Internet Protocol(IP) networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.

---

## Why ?
Assigning IP for every device is very tedious task. Also If device is turned off and IP is not revoked then that IP is wasted. This way we can run out of IP's that can assign in network . Also If IP is self assign then mistakes of same IP for two devices can be there.

---

## How DHCP assigns IP?
DHCP servers assign IP address from a range of IP's to device on lease.
Mostly follows what's called DORA Process 

|Process|Work|
|:-|:-|
|DHCP **D**iscover | Looks for DHCP server|
|DHCP **O**ffer |server offers IP|
|DHCP **R**equest|Host requests to lease that IP|
|DHCP **A**cknowledgement |Server assigns IP , subnet mask and lease time|

![DHCP working](https://forum.huawei.com/enterprise/en/data/attachment/forum/202003/12/113904og7bm2c50i593yqy.png?26.png)

Ports use for DHCP communication :
- Clients : port 68
- Server : port 67
- UDP protocol

---

## DHCP messsage format

![DHCP message format](https://www.researchgate.net/profile/Jaeseung-Song/publication/263813522/figure/fig10/AS:667882941866005@1536247110658/Packet-format-for-DHCP.png)

If DHCP fails then windows has backup plan called [APIPA](APIPA.md)
If DHCP server is not in same network then we need to set relay agent which will act as mailman for communication.
To check if address is alotted , it pings devices. If reply gets to DHCP server and conflict is found then server automatically removes that IP from server pool.

---

### Sources
- [DHCP Youtube](https://youtu.be/e6-TaH5bkjo)
- [DHCP working Youtube](https://youtu.be/S43CFcpOZSI)
- [Wikipedia](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)