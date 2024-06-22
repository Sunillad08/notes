# Footprinting & Scanning

[Back](../index.md)

-- -

# Network Mapping

Prerequisite: [IP](../../Networking/Protocols/IP.md), [ICMP](../../Networking/Protocols/ICMP.md), [IPv4](../../Networking/Protocols/IPv4.md), [IPv6](../../Networking/Protocols/IPv6.md), [TCP](../../Networking/Protocols/TCP.md), [UDP](../../Networking/Protocols/UDP.md), [TCP_IP_3_way_handshake](../../Networking/TCP_IP_3_way_handshake.md)

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


### Read [nmap](../../Cyber_Security/Tools/nmap.md) to learn about host discovery using ICMP sweep, ARP sweep and multiple other ways.

-- -

# Port Scanning

## Port Scanning

Port scanning using [nmap](../../Cyber_Security/Tools/nmap.md).

Use Stealth scan to avoid getting detected. Use TCP scan in verification.

Use -Pn to avoid sending ping to system and clarify nmap not to verify if host is up or not.

Use -p- to scan all possible port range.

Use timing templates to adjust scan duration and avoid detection.

Once all open ports are identified, we can move on to service version and OS detection.

## Service Version & OS Detection

Use [nmap](../../Cyber_Security/Tools/nmap.md) to gather information regarding service versions and OS of machine. After detecting active machines, its better to perform OS detection before port detection so you target specific ports. After detecting open ports , perform service version detection on found open port.

Use -sV for version detection on open ports. 
Provide open ports number to perform scan faster.

Use -O for detection of host operating system.
Use '--osscan-guess' to get more info if nmap is not giving proper output.

Use -sC for running nmap scripts for further enumeration

-- -

#  Evasion : Firewall , IDS & other security measures

Read [nmap](../../Cyber_Security/Tools/nmap.md) and [Nmap Documentation](https://nmap.org/book/man-bypass-firewalls-ids.html).

If pings are blocked or scans are getting timeout, that indicates presence of firewall , IDS or other security measures. To avoid getting detected we can apply few methods.

### Packet fragmentation
Using `-f` and `--mtu` option in nmap to sent fragmented packets and set custom MTU ( Maximum Transmission Unit ). 

### Decoy IP 
We can set decoy IPs to avoid repeating or revealing our own IP address. We need to have either network logs or access to decoy machines to fetch response. We can use `-D` flag in nmap to set multiple decoy IPs.

### Port Number
We can also spoof port number from our end to evade firewall blocking request from repeative port number. We can use `-g` option in nmap to spoof port number.

### Spoof IP
In some circumstances, Nmap may not be able to determine your source address. In this situation, use `-S` with the IP address of the interface you wish to send packets through. This is replace spoofed IP in place of actual.

## Optimising nmap

Optimizing Nmap scan is also important as getting result in short time while creating less traceable traffic is necessary. We should use timing template to red

We can use `--host-timeout 5s` to reduce timeout value. We can also delay scan to avoid flooding systems with `--scan-delay`.
