# Wifi Security
[Back to cyber security page](Cyber%20security.md)
- --
## WEP
**Wired Equivalent Privacy**
**WEP** was developed for wireless networks and approved as a Wi-Fi security standard in September 1999. WEP was supposed to offer the same security level as wired networks, however there are a lot of well-known security issues in WEP, which is also easy to break and hard to configure.

Despite all the work that has been done to improve the WEP system it still is a highly vulnerable solution. Systems that rely on this protocol should be either upgraded or replaced in case security upgrade is not possible. WEP was officially abandoned by the Wi-Fi Alliance in 2004.
- --
## WAP
**Wi-Fi Protected Access**
For the time the 802.11i wireless security standard was in development, WPA was used as a temporary security enhancement for WEP. One year before WEP was officially abandoned, WPA was formally adopted. Most modern WPA applications use a pre-shared key (PSK), most often referred to as WPA Personal, and the Temporal Key Integrity Protocol or TKIP for encryption. WPA Enterprise uses an authentication server for keys and certificates generation.

WPA was a significant enhancement over WEP, but as the core components were made so they could be rolled out through firmware upgrades on WEP-enabled devices, they still relied onto exploited elements.

WPA, just like WEP, after being put through proof-of-concept and applied public demonstrations turned out to be pretty vulnerable to intrusion. The attacks that posed the most threat to the protocol were however not the direct ones, but those that were made on Wi-Fi Protected Setup (WPS) - auxiliary system developed to simplify the linking of devices to modern access points.
- --
## WAP 2
The 802.11i wireless security standard based protocol was introduced in 2004. The most important improvement of WPA2 over WPA was the usage of the Advanced Encryption Standard (AES). AES is approved by the U.S. government for encrypting the information classified as top secret, so it must be good enough to protect home networks.

At this time the main [vulnerability to a WPA2](https://www.netspotapp.com/krack-wifi-vulnerability-wpa2.html) system is when the attacker already has access to a secured WiFi network and can gain access to certain keys to perform an attack on other devices on the network. This being said, the security suggestions for the known WPA2 vulnerabilities are mostly significant to the networks of enterprise levels, and not really relevant for small home networks.

Unfortunately, the possibility of attacks via the Wi-Fi Protected Setup (WPS), is still high in the current WPA2-capable access points, which is the issue with WPA too. And even though breaking into a WPA/WPA2 secured network through this hole will take anywhere around 2 to 14 hours it is still a real security issue and WPS should be disabled and it would be good if the access point firmware could be reset to a distribution not supporting WPS to entirely exclude this attack vector.
- --
## WAP 3
Wi-Fi Alliance announced WPA3 security protocol in 2018, which provides a much more secure and reliable method replacing WPA2 and the older security protocols. The fundamental shortcomings of WPA2 like imperfect four-way handshake and using a PSK (pre-shared key) causes your Wi-Fi connections to become exposed to compromise. WPA3 has further security improvements that make it harder to break into networks by guessing passwords
- --
### Source
- [Website](https://www.netspotapp.com/blog/wifi-security/wifi-encryption-and-security.html)
- [WPA 3 Website](https://www.asus.com/us/support/FAQ/1042478)