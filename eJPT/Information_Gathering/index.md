# Information Gathering
[Back](../index.md)

-- -

Quick Access:
- [Passive Information Gathering](#Passive%20Information%20Gathering)
- [Active Information Gathering](#Active%20Information%20Gathering)

## Information Gathering

Information gathering refers to gathering or collecting information about person, company and system that you're targeting.

### Types of Information Gathering:
- **Active Information Gathering** : Gathering information with engagement with system.
- **Passive Information Gathering** : Gathering information available in public domain without engaging with systems.

### What information to collect?
- Passive : IP address, DNS details, Email address, Web technology, subdomains, etc.
- Active : Open ports, internal infrastructure of target, information about target systems.


-- -
# Passive Information Gathering

## Web Recon and Footprinting

Web reconnaissance  and footprinting focusses on gathering information about website.

- Whatis \<host\>
- robots.txt
- sitemap.xml or sitemaps.xml
- Builtwith and wappalyzer : To identify web technologies used
- Whatweb : Command line utility to gather technology information
- HTTrack (app) webhttrack (cmd) : To download and replicate website in local environment

## Domain Information gathering

Read [DNS](../../Networking/Protocols/DNS.md)

### Whois
Command line tool to gather DNS information about host
```
Whois hostname
```
- Who.is : Web version of Whois

### Netcraft 
- Sitereport.netcraft.com to gather DNS , Web technologies and Firewall information.

### DNSRecon 
To find information regarding domain

```
DNSRecon -d domain_name
```

- dnsdumpster.com (Website)

### CRT.sh : 
Gather information about subdomains on basis of certificates.

### Sublist3r
To identify subdomains of given domain
```
Sublist3r domain_name
```

## Web Application Firewall(WAF) detection 
To detect web application firewall being used.
 
```
waffw00f domain
``` 

## Google Dork

Read [Google_Dorking](../../Cyber_Security/Tools/Google_Dorking.md)

examples : 
Site:
Intitle : index of
Cache: site_name


### Google Hacking Database (GHDB)
Interesting google dorks stored in database.

## Wayback machine
To check previous versions of websites and find information from it.


## Email Harvesting

### theHarvester
- Helps in OSINT.
- Command line tool
- help to find emails , subdomains and IPs


## Leaked password

### haveibeenpwned.com
To find leaked passwords in breaches, gather information about possible breaches occured.


-- -

# Active Information Gathering

Read [DNS](../../Networking/Protocols/DNS.md)

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