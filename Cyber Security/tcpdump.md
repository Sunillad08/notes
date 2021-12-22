# tcpdump
[Back to cyber security page](Cyber%20security.md)
- --
## What is tcpdump?
tcpdump (8)          - dump traffic on a network
tcpdump is used to track traffic in network.
Basically command line [Wireshark](Wireshark.md).
- --
## tcpdump syntax
```bash
tcpdump [ -AbdDefhHIJKlLnNOpqStuUvxX# ] [ -B buffer_size ]
               [ -c count ] [ --count ] [ -C file_size ]
               [ -E spi@ipaddr algo:secret,...  ]
               [ -F file ] [ -G rotate_seconds ] [ -i interface ]
               [ --immediate-mode ] [ -j tstamp_type ] [ -m module ]
               [ -M secret ] [ --number ] [ --print ] [ -Q in|out|inout ]
               [ -r file ] [ -s snaplen ] [ -T type ] [ --version ]
               [ -V file ] [ -w file ] [ -W filecount ] [ -y datalinktype ]
               [ -z postrotate-command ] [ -Z user ]
               [ --time-stamp-precision=tstamp_precision ]
               [ --micro ] [ --nano ]
               [ expression ]
```
- --
Options
```bash
-X : Show the packet’s contents in both hex and ascii.
-XX : Same as -X, but also shows the ethernet header.
-D : Show the list of available interfaces
-l : Line-readable output (for viewing as you save, or sending to other commands)
-q : Be less verbose (more quiet) with your output.
-t : Give human-readable timestamp output.
-tttt : Give maximally human-readable timestamp output.
-i eth0 : Listen on the eth0 interface.
-vv : Verbose output (more v’s gives more output).
-c : Only get x number of packets and then stop.
-s : Define the snaplength (size) of the capture in bytes. Use -s0 to get everything, unless you are intentionally capturing less.
-S : Print absolute sequence numbers.
-e : Get the ethernet header as well.
-q : Show less protocol information.
-E : Decrypt IPSEC traffic by providing an encryption key.
```
Read [site](https://danielmiessler.com/study/tcpdump/) for more information.
- --
### Source 
- [Website](https://danielmiessler.com/study/tcpdump/)
- Man page of tcpdump