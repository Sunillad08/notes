# PAT
[Back to networking page](index.md)
- --
## What is PAT?
PAT stands for port address translation. It’s a type of dynamic NAT, but it bands several local IP addresses to a singular public one. Organizations that want all their employees’ activity to use a singular IP address use a PAT, often under the supervision of a network administrator.
- --
## How PAT works?
Each private IP + Port number  is mapped to port of public IP.
Example:
192.168.0.2:80 -> 1.2.3.4:10
192.168.0.5:80 -> 1.2.3.4:11
192.168.0.8:80 -> 1.2.3.4:12
192.168.0.8:85 -> 1.2.3.4:13

![PAT|700](https://qph.fs.quoracdn.net/main-qimg-61f8d3d6d39bcce4f1398a319aa2775a)
- --
### Source
- [Youtube video](https://youtu.be/awFk_CN9SNs)