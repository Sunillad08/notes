# Footprinting & scanning
[Back to cyber security page](./index.md)

---

## Mapping network & scanning targets
- By mapping networks , we can get insights of connected network and current running devices and there ip addresses.
- We can scan each machine to find details about OS so we can get idea about what system are there. Also finger printing OS , we can search vulnerabilities about system by even googling.
- **Getting permission is MUST**
- **Scanning network without permission is cyber OFFENCE**


---

### How to do scanning?
First we need ip of network to scan.
- Ping
	- ping 192.168.0.1
	- Pinging is utility that is designed to test if a machine is live.
	- Pinging sents ICMP packets , if we get echo reply then host is alive
	- --
- Fping
	- fping -a -g 192.168.0.1/24
	- fping -a -g 192.168.0.1 192.186.0.100
	- Fping is linux tool which is improved ping . We can sweep ping ip's.
	- --
- nmap
	- nmap -sn 192.168.0.1
	- [More about nmap](nmap.md)

---


## Port scanning methods

### TCP Port scanner
[TCP_IP_3_way_handshake](../Networking/TCP_IP_3_way_handshake.md)

---

**About [TCP](../Networking/TCP.md)**
**TCP Full Scan**
- To detect if port is open If 3 way handshake is completed then we send RST + ACK packet to close connection.
- If after SYN request we get RST + ACK from server then port is closed.
- Although this type of scan will be easily detected & also recorded in logs as many connection coming from one device can be blocked. 
- namp -sT 192.168.0.125
![TCP SYN scan | 600](https://static.packt-cdn.com/products/9781788995177/graphics/cee1f406-7dec-4e44-8312-faf9075f803c.png)

---

**TCP SYN Scan**
- Stealthy scan is another name.
- It only send SYN and analyzes response coming back form target machine
- If RST then port is closed and ACK then port is open(Sends RST to stop handshake).
- namp -sS 192.168.0.125
![TCP SYN scan | 600](https://static.packt-cdn.com/products/9781788995177/graphics/d4140e2f-98ec-4859-89f2-81e2abc92aaf.png)
- --
**About [UDP](../Networking/UDP.md)**
**UDP Scan**
- UDP scans are slower
- If reponse is ICMP packet then port is closed
- If reponse is not there then open|filtered
- As UDP is connection-less so determining state is tough

---

## OS Fingerprinting
### What is OS fingerprinting
- OS fingerprinting means getting knowledge about OS . 
- By getting approx knowledge about OS , we can find vulnerabilities based on version and security level of OS.

### Tools:
- nmap 
	- nmap -O 192.168.0.2
	- [More about nmap](nmap.md)

---


### Sources :
- [ine](https://my.ine.com/CyberSecurity/courses/6f986ca5/penetration-testing-basics)