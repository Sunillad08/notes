# DNS Enumeration
[Back to cyber security page](./index.md)

---

## What is DNS Enumeration?
DNS enumeration is the process of locating all the [DNS](../Networking/Protocols/DNS.md) servers and their corresponding records for an organization.

It gives up information about IP adddress and internal and external DNS

---

## DNS Information

|Types|Use|
|:--|:-|
|A (Address)| Maps a hostname to an IP address |
|SOA (Start of Authority)|Identifies the DNS server responsible for the domain information|
|CNAME (Canonical Name)| Provides additional names or aliases for the address record |
|MX (Mail Exchange)|Identifies the mail server for the domain|
|SRV (Service) |Identifies services such as directory services|
|PTR (Pointer) |Maps IP addresses to hostnames |
|NS (Name Server)|Identifies other name servers for the domain|
|TXT (Text) | Add Text data in DNS Records

---

## How to do it?
1. nslookup : query Internet name servers interactively
nslookup example.com
```
Server:         192.168.0.1
Address:        192.168.0.1#53

Non-authoritative answer:
Name:   example.com
Address: 93.184.216.34
Name:   example.com
Address: 2606:2800:220:1:248:1893:25c8:1946
```

2. whois : information about domain registration
whois example.com
```
Domain Name: EXMAPLE.COM
Registry Domain ID: 132185704_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.cloudflare.com
Registrar URL: http://www.cloudflare.com
Updated Date: 2021-07-11T11:00:02Z
Creation Date: 2004-10-08T13:53:42Z
Registry Expiry Date: 2022-10-08T13:53:42Z
Registrar: CloudFlare, Inc.
Registrar IANA ID: 1910
Registrar Abuse Contact Email:
Registrar Abuse Contact Phone:
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
ttps://icann.org/epp#clientTransferProhibited
Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
Name Server: ARA.NS.CLOUDFLARE.COM
Name Server: JAY.NS.CLOUDFLARE.COM
DNSSEC: signedDelegation
DNSSEC DS Data: 2371 13 2 072EEC16F225F954BCF4DE9DB653B3413D2F03B362B1C580EC4C732A652D7F71
URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
 ```
 
3. dig : DNS lookup utility
dig example.com    
```
; <<>> DiG 9.16.15-Debian <<>> example.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 48107
;; flags: qr rd ra ad; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;example.com.                   IN      A

;; ANSWER SECTION:
example.com.            9097    IN      A       93.184.216.34

;; Query time: 4 msec
;; SERVER: 192.168.0.1#53(192.168.0.1)
;; WHEN: Sat Nov 13 19:25:05 IST 2021
;; MSG SIZE  rcvd: 56

```

4.  traceroute / tracert
traceroute example.com
```
traceroute to example.com (93.184.216.34), 30 hops max, 60 byte packets
 1  192.168.0.1 (192.168.0.1)  1.960 ms  2.022 ms  2.000 ms
 2  172.22.11.163 (172.22.11.163)  3.579 ms  3.554 ms  3.537 ms
 3  172.22.11.129 (172.22.11.129)  4.464 ms  4.759 ms  4.740 ms
 4  nsg-corporate-149.212.187.122.airtel.in (122.187.212.149)  6.961 ms  6.908 ms  6.897 ms
 5  182.79.154.0 (182.79.154.0)  128.471 ms  128.307 ms  128.301 ms
 6  ldn-b7-link.ip.twelve99.net (62.115.175.230)  129.550 ms  132.700 ms  133.056 ms
 7  ldn-bb4-link.ip.twelve99.net (62.115.141.246)  133.035 ms ldn-bb1-link.ip.twelve99.net (62.115.138.168)  131.014 ms ldn-bb4-link.ip.twelve99.net (62.115.141.246)  129.822 ms
 8  nyk-bb2-link.ip.twelve99.net (62.115.113.20)  220.421 ms  220.846 ms nyk-bb1-link.ip.twelve99.net (62.115.112.244)  226.456 ms
 9  nyk-b1-link.ip.twelve99.net (62.115.135.131)  220.197 ms  216.233 ms nyk-b1-link.ip.twelve99.net (62.115.135.133)  221.434 ms
10  edgecast-ic317660-nyk-b6.ip.twelve99-cust.net (62.115.147.201)  221.404 ms  205.776 ms edgecast-ic317659-nyk-b6.ip.twelve99-cust.net (62.115.147.199)  207.768 ms
11  ae-70.core1.nyb.edgecastcdn.net (152.195.68.141)  208.286 ms  209.446 ms ae-71.core1.nyb.edgecastcdn.net (152.195.69.139)  209.363 ms
12  93.184.216.34 (93.184.216.34)  210.103 ms  208.405 ms  209.647 ms
13  93.184.216.34 (93.184.216.34)  207.634 ms  207.609 ms  210.572 ms
```

5. dnsdumpster.com
https://dnsdumpster.com/
Check details about DNS data and overall data.

---

### Source
- [Tryhackme](https://tryhackme.com/room/passiverecon)
- [hsploit Youtube video](https://youtu.be/rQ-dc5kwRtU)
- [Youtube video]()