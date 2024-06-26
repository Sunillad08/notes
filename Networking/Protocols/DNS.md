# DNS : Domain Name System
[Back to networking page](../index.md)

---

## What is DNS?
DNS is **Domain Name System** which converts domain name to IP addresses.
Domain names -> [IP](IP.md)
Example : play.google.com -> 185.056.012.155

The Domain Name System is a hierarchical and decentralized naming system for computers, services, or other resources connected to the Internet or a private network. It associates various information with domain names assigned to each of the participating entities.

Port 53 is used. UDP is used. Total 128 levels and level 0 is root.
Root label is empty , each node has name(maximum 63 characters) .

---

## Why?
DNS is phonebook of Internet. Domain name is searched and they return IP. Remebering numerical values that changes frequently is not the best way to remember any website. DNS is used to resolve domain names to IP's so that we only have to remember articular string.

---

## Name Architectures
**Flat name architecture : ** 
There is no clear relationship between names .

**Hierarchical Name Architecture : **
There is defined relationship between names spaces.


---

## Types of DNS

### Root Name Server
A root server accepts a recursive resolver’s query which includes a domain name, and the root nameserver responds by directing the recursive resolver to a TLD nameserver, based on the extension of that domain (.com, .net, .org, etc.). 13 Root name server(a-m).

### TLD Name server (Top level domain)
A TLD nameserver maintains information for all the domain names that share a common domain extension, such as .com, .net, or whatever comes after the last dot in a url. For example, a .com TLD nameserver contains information for every website that ends in ‘.com’. If a user was searching for google.com, after receiving a response from a root nameserver, the recursive resolver would then send a query to a .com TLD nameserver, which would respond by pointing to the authoritative nameserver for that domain.

### Authoritative name server
When a recursive resolver receives a response from a TLD nameserver, that response will direct the resolver to an authoritative nameserver. The authoritative nameserver is usually the resolver’s last step in the journey for an IP address. The authoritative nameserver contains information specific to the domain name it serves (e.g. google.com) and it can provide a recursive resolver with the IP address of that server found in the DNS A record, or if the domain has a CNAME record it will provide the recursive resolver with an alias domain, at which point the recursive resolver will have to perform a whole new DNS lookup to procure a record from an authoritative nameserver (often an A record containing an IP address).

### Primary server 
It is server which stores file about its zone. I tis authorized to create , maintain and update the zone filie. 

### Secondary server 
It is used for backup to primary server , it doesn't have authority to create or update zone file.

---

## How does DNS work?

![DNS Working](http://www.tcpipguide.com/free/diagrams/dnsresolution.png)

- DNS resolver checks its cache for IP address.
- If not found then DNS query is sent by DNS resolver to root name server. 
- Root name server then checks domain extention such as .com or .net
- Root name server returns IP of Top level domain server.
- Top level domain receives request from DNS resolver.
- TLD server returns IP of Authoritative name server.
- DNS resolver sends request to Authoritative name servers
- Authoritative name servers returns with IP.

---

## DNS in Internet

1. **Generic domains** : Generic domains are defined from categories like .com or .gov .
2. **Country domain** : Country domain are created using two character country name abbreviation like .in , .us .
3. **Inverse Domain** : Used for mapping IP address to a name for reverse resolution like 121.52.5.8.in_addr_.arpa .

![DNS in internet](https://www.tutorialride.com/images/computer-network/dns-in-internet.jpeg)

---

## DNS Message format
1. Query : Header and question section
2. Response : Query message + Answer section + authoritative section + Additonal section information

![Message format](https://i.imgur.com/68escU5.png)

---

### DNS Record types

![DNS Record types](https://en.wikipedia.org/wiki/List_of_DNS_record_types#/media/File:All_active_dns_record_types.png)

A - Resolves hostname to IPv4
AAAA - Resolves hostname to IPv6
NS - Reference to Domain name server
MX - Mail server
CNAME - domain alias
TXT - text records
SOA - Domain authority 
SRV - Service records
PTR - IP address to hostname

### Sources
- [Wiki](https://en.wikipedia.org/wiki/Domain_Name_System)
- [Cloud flare](https://www.cloudflare.com/en-in/learning/dns/dns-server-types/)
- [Youtube 1](https://youtu.be/JkEYOt08-rU)
- [Youtube 2](https://youtu.be/FsGUi5pXpLk)
- [Youtube 3](https://www.youtube.com/watch?v=uOfonONtIuk)
- [Youtube 4](https://youtu.be/Rck3BALhI5c)
- [Youtube 5](https://youtu.be/mpQZVYPuDGU)