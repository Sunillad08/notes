# ICMP
[Back to Networking page](index.md)
- --
## What is ICMP?
The **Internet Control Message Protocol** (ICMP) is a supporting protocol in the Internet protocol suite. It is used by network devices, including routers, to send error messages and operational information indicating success or failure when communicating with another IP address, for example, when an error is indicated when a requested service is not available or that a host or router could not be reached. 

ICMP differs from transport protocols such as TCP and UDP in that it is not typically used to exchange data between systems, nor is it regularly employed by end-user network applications (with the exception of some diagnostic tools like ping and traceroute).

- --
## ICMP Headers
![ICMP|700](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2Fo_t2kyR404k%2Fmaxresdefault.jpg&f=1&nofb=1)

- Type : ICMP type, see Control messages.
- Code : ICMP subtype, see Control messages.
- Checksum : Internet checksum (RFC 1071) for error checking, calculated from the ICMP header and data with value 0 substituted for this field.
- Rest of header : Four-byte field, contents vary based on the ICMP type and code.

For control messages , check this [Wikipedia page](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol#Control_messages)
- --
### Source:
- [Wiki](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol)
- [Youtube video](https://youtu.be/RF_Qafg7PGI)
- [Englist YT Video](https://youtu.be/xTqtm7-k25o)