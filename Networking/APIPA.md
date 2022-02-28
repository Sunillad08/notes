# APIPA
[Back to networking page](./index.md)

---

## What is APIPA?
**Automatic Private IP Addressing**
Automatic Private IP Addressing (APIPA) is a feature of _Windows-based operating systems_ (included in Windows 98, ME, 2000, and XP) that enables a computer to automatically assign itself an IP address when there is no Dynamic Host Configuration Protocol (DHCP) server available to perform that function.

---

## Why?
If [DHCP](DHCP.md) server fails then it can assign itself IP from  169.254.0.0/16 (_169.254.0.0_ through _169.254.255.255_) and subnet mask of 255.255.0.0.
Now Device can connect with internal devices only. **NO INTERNET**
Device need to broadcast [ARP](ARP.md) message so other won't pick up same IP.
Continuously searches for DHCP over time for valid IP.

![APIPA](https://media.geeksforgeeks.org/wp-content/uploads/20200428145226/APIPA_21.png)


---

## Sources
- [Wiki](https://en.wikipedia.org/wiki/Link-local_address)
- [Short Youtube](https://youtu.be/0tEjUR6tjBU)
- [geeksforgeeks](https://www.geeksforgeeks.org/what-is-apipa-automatic-private-ip-addressing/)