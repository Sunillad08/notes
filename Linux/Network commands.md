# Network Commands 
[Back to linux page](Linux.md)
- --
## IP related commands
ip : show ip of device
ip a , ip add , ip address

ifconfig : shows network and connections and manage them
ifconfig , ifconfig < network> down/up

host : shows ip or domain name
host google.com

iwconfig : manage wireless network connections
iwconfig

netstat : Display connection information.
netstat -t , netstat -r

netdiscover : active/passive ARP reconnaissance tool
netdiscover -i eth0

ss : Investigate sockets
ss , ss -s

- --
## Connectivity related commands

ping : ping particular network or device
ping 192.168.0.108 , ping -c 4 192.168.0.1

traceroute : shows path packets follow an amount of time it takes
traceroute fb.com

- --
## DNS related commands

nslookup : DNS related queries
nslookup google.com

dig : check ip of domain , DNS related information
dig google.com

- --
## Downloading files from internet
wget : download file from internet
wget link

curl : download file directly
curl link

- --
## Info about website
whois : gets info about website
whois google.com

- --
## DHCP 
dhclient : command to run dhcp related commands
dhclient -4
- --
### Sources
- [Java point website](https://www.javatpoint.com/linux-networking-commands)
- [Ping & traceroute](https://www.youtube.com/watch?v=vJV-GBZ6PeM&list=WL&index=50&ab_channel=PowerCertAnimatedVideos)