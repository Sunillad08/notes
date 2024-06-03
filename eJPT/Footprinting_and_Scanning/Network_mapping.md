# Network Mapping
[Back](./index.md)

-- -

Prerequisite: [IP](../../Networking/IP.md), [ICMP](../../Networking/ICMP.md), [IPv4](../../Networking/IPv4.md), [IPv6](../../Networking/IPv6.md), [TCP](../../Networking/TCP.md), [UDP](../../Networking/UDP.md), [TCP_IP_3_way_handshake](../../Networking/TCP_IP_3_way_handshake.md)

## Objective
- Discovery of live hosts
- Identify open ports and services
- Network topology mapping
- OS fingerprinting
- service version detection
- identify filtering and security measures

> [nmap](../../Cyber_Security/Tools/nmap.md) is predominantly used for network mapping and diagnostics.


## Command to check all open TCP connections
```bash
Linux> Netstat  -antp
```

```powershell
Windows> Netstat -ano
```


## Host discovery technique 
- ping sweeps / ICMP Ping
	- Firewall may block ICMP packets
- Arp scanning 
- TCP SYN scan
	- Firewall/Security measures may block
- UDP ping
- TCP ACK
- SYN ACK







