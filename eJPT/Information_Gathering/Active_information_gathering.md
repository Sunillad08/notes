# Active Information Gathering

[Back](./index.md)

-- -

Read [DNS](../../Networking/Protocols/DNS.md)

-- -

## DNS Zone Transfer

DNS Zone Transfer : Process of copy or transfer of zone files from one DNS server to another.

![DNS Zone Transfer](https://images.ctfassets.net/aoyx73g9h2pg/1PGX1tDUWI2LvZaMfcuLLD/f98d47c3d88a0756e6d13884fec69628/What-are-DNS-zone-transfers-Diagram.jpg)

- [DNS Zone Transfer Hackersploit](https://youtu.be/kdYnSfzb3UA?si=lxAt7FEex7ZcDcKv)
- [DNS Zone Transfer Hindi](https://youtu.be/4-vKfKVyjHA?si=HmQssVkYpXaDXsOS)

-- -

## dig
DNS Zone Transfer using dig
```
dig axfr @"nameserver" "site"
```


## dnsenum
Enumeration of publically available information, zone transfer and bruteforce subdomains.
```
dnsenum "site"
```


## fierce 

```
fierce –dns domain_name
```


## Nmap

Read [nmap](../../Cyber_Security/Tools/nmap.md) , [hping3](../../Cyber_Security/Tools/hping3.md)

To enumerate active machines using ping scan to gather active machines IP.
