# SCTP
[Back to networking page](./index.md)

---

## What is SCTP
Stream Control Transmission Protocol (SCTP) is a transport-layer protocol that ensures reliable, in-sequence transport of data. SCTP provides multihoming support where one or both endpoints of a connection can consist of more than one IP address. This enables transparent failover between redundant network paths.

Benefits of both TCP and UDP.

SCTP is message oriented , reliable protocol.

Full Duplex Communication.

---
## Multiple Stream
Unlike TCP , SCTP can have multiple streams to transfer data which is helpful as in TCP if stream is delayed or blocked then connection fails. SCTP having multiple stream can be useful to tranfer real-time data with reliability. 

![SCTP Multiple stream](https://slidetodoc.com/presentation_image_h/b5cd43dfbedade2adb97760947f65708/image-4.jpg)

---

## Multihoming in SCTP
The ability of an endpoint to support multiple IP addresses is known as multihoming, which means SCTP can transmit to an alternative IP address belonging to the endpoint in case of a network failure or adverse conditions.

![Multihoming SCTP](https://oriolrius.cat/article_fitxers/1838/Better%20networking%20with%20SCTP_files/figure2.gif)

---

## SCTP Header

![SCTP Header](https://www.researchgate.net/profile/Esbold-Unurkhaan-2/publication/220144818/figure/fig1/AS:276798165274627@1443005233789/SCTP-packet-format-with-common-header-und-chunks.png)

 - Source port address : 16-bit field that defines the port number of the process sending the packet.
- Destination port address : 16-bit field that defines the port number of the process receiving the packet.
- Verification tag : This is a number that matches a packet to an association. This prevents a packet from a previous association from being mistaken as a packet in this association. It serves as an identifier for the association; it is repeated in every packet during the association. There is a separate verification used for each direction in the association.
- Checksum : 32-bit field contains a CRC-32 checksum

For chunk header :
- Type. This 8-bit field can define up to 256 types of chunks. Only a few have been defined so far; the rest are reserved for future use.
- Flag. This 8-bit field defines special flags that a particular chunk may need. Each bit has a different meaning depending on the type of chunk.
- Length. Since the size of the information section is dependent on the type of chunk, we need to define the chunk boundaries. This 16-bit field defines the total length.

---
## SCTP Handshake

![SCTP](https://www.juniper.net/documentation/us/en/software/junos/gtp-sctp/images/g034207.gif)

1. INIT Chunk
2. INIT_ACK Chunk
3. COOKIE_ECHO Chunk
4. COOKIE_ACK Chunk

---

## Source :
- [Ekeeda Youtube video](https://youtu.be/TwBH14AWtqw)
- [Juniper net SCTP](https://www.juniper.net/documentation/us/en/software/junos/gtp-sctp/topics/topic-map/security-gprs-sctp.html#:~:text=Stream%20Control%20Transmission%20Protocol%20(SCTP)%20is%20a%20transport%2Dlayer,failover%20between%20redundant%20network%20paths.)