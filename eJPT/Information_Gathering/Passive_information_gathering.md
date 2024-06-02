# Passive Information Gathering
[Back](./index.md)

-- -

## Web Recon and Footprinting

Web reconnaissance  and footprinting focusses on gathering information about website.

- Whatis \<host\>
- robots.txt
- sitemap.xml or sitemaps.xml
- Builtwith and wappalyzer : To identify web technologies used
- Whatweb : Command line utility to gather technology information
- HTTrack (app) webhttrack (cmd) : To download and replicate website in local environment

## Domain Information gathering

Read [DNS](../../Networking/DNS.md)

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