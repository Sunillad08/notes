# netcat
[Back to cyber security page](../index.md)

---

## What is netcat?
**TCP/IP swiss army knife**

The Netcat utility program supports a wide range of commands to manage networks and monitor the flow of traffic data between systems. Computer networks, including the world wide web, are built on the backbone of the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP).  Think of it as a free and easy companion tool to use alongside Wireshark, which specializes in the analysis of network packets. The original version of Netcat was released back in 1995 and has received a number of iterative updates in the decades since.

---

## flags
connect to somewhere:   nc -options hostname port ports ... 
listen for inbound:     nc -l -p port -options hostname port
options:
```bash
-c shell commands       as `-e'; use /bin/sh to exec [dangerous!!]
-e filename             program to exec after connect [dangerous!!]
-b                      allow broadcasts
-g gateway              source-routing hop point[s], up to 8
-G num                  source-routing pointer: 4, 8, 12, ...
-h                      this cruft
-i secs                 delay interval for lines sent, ports scanned
-k                      set keepalive option on socket
-l                      listen mode, for inbound connects
-n                      numeric-only IP addresses, no DNS
-o file                 hex dump of traffic
-p port                 local port number
-r                      randomize local and remote ports
-q secs                 quit after EOF on stdin and delay of secs
-s addr                 local source address
-T tos                  set Type Of Service
-t                      answer TELNET negotiation
-u                      UDP mode
-v                      verbose [use twice to be more verbose]
-w secs                 timeout for connects and final net reads
-C                      Send CRLF as line-ending
-z                      zero-I/O mode [used for scanning]
```
port numbers can be individual or ranges: lo-hi [inclusive];
hyphens in port names must be backslash escaped (e.g. 'ftp\-data').

---

### Source
- [Website](https://www.varonis.com/blog/netcat-commands/)
- [Youtube video](https://youtu.be/VF4In6rIPGc)
- [Youtube video hindi](https://youtu.be/Wzc9cgEar7g)
