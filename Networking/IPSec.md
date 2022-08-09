# IPSec
[Back to networking page](./index.md)

---

## What is IPSec ?
IPSec stands for Internet Protocol Security protocol which provides source authentication , confidentiality and Privacy.

IPsec is a group of protocols that are used together to set up encrypted connections between devices. It helps keep data sent over public networks secure.

---

## Modes of IPSec

There are two modes of IPSec

1. Transport Mode :
In Transport mode , only data payload (Transport layer data) is encapsulated in IPSec header anb trailer. IP header is not protected. 

||
|:--:|
|Transport Layer|
|**IPSec Layer**|
|Network Layer|

2. Tunnel Mode :
In tunnel mode , both IP header and data are encapsulated within IPSec header and trailer. 

||
|:--:|
|Transport Layer|
|Network Layer|
|**IPSec Layer**|
|New Network Layer|

|Network Layer|

![IPSec modes](https://www.researchgate.net/profile/Nikos-Mastorakis/publication/241773831/figure/fig2/AS:411264229625856@1475064441019/Tunnel-vs-Transport-Mode-IPSec.png)

---

## Two Security Protocols

1. Authentication Header (AH)
2. Encapsulation Security Payload (ESP)

---

## Authentication Header

**The AH protocol provides source authentication and data integrity, but not privacy.**

![AH Header format](https://www.researchgate.net/profile/Riaz-Khan-19/publication/297336095/figure/fig1/AS:558684921135104@1510212273046/Authentication-Header-Format.png)

*IP header protocol field is changed to protocol 51*

- Next Header : 8 bit field which defines what payload is carried by IP packet.
- Payload length : Payload length is length of AH Header in 4 bytes multiple , **first 8 bytes of data are not included for calculation of this**.
- Reserved : Reserved for future use
- Security Parameter Index (SPI) : Security parameter index is 32 bit unique identifier with role of a virtual circuit identifier and is the same for all packets sent during a connection called a Security Association.
- Sequence Number : Sequence number is 32 bit field to identify ordering of packet. Sequence number is not repeated for retransmission and new connection is required when it reaches 2\*\*32 (no wrap around to zero) .
- Authentication Data : Authentication data field is the result of applying a hash function to the entire IP datagram except for the fields that are changed during transit (TTL and Checksum).


---

## Encapsulation Security Payload

**ESP provides source authentication, data integrity, and privacy.**

![ESP header](https://www.researchgate.net/profile/Nor-Effendy-Othman/publication/266477318/figure/fig6/AS:392207388430356@1470520936898/Encapsulated-Security-Payload-ESP-protocol-in-transport-mode.png)

*IP header protocol field is changed to protocol 50*

Header
- Security Parameter Index (SPI) : Security parameter index is 32 bit unique identifier with role of a virtual circuit identifier and is the same for all packets sent during a connection called a Security Association.
- Sequence Number : Sequence number is 32 bit field to identify ordering of packet. Sequence number is not repeated for retransmission and new connection is required when it reaches 2\*\*32 (no wrap around to zero) .

Trailer
- Next Header : 8 bit field which defines what payload is carried by IP packet.
- Pad length : 8-bit pad-length field defines the number of padding bytes. The value is between 0 and 255.

- Authentication Data : authentication data field is the result of applying an authentication scheme to parts of the datagram. Note the difference between the authentication data in AH and ESP. In AH, part of the IP header is included in the calculation of the authentication data; in ESP, it is not.

---

## Source :
- [WIkipedia](https://en.wikipedia.org/wiki/IPsec)
- [Cloudflaire](https://www.cloudflare.com/en-in/learning/network-layer/what-is-ipsec/)
- TCP IP by Farouzan