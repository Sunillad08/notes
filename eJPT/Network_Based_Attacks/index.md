# Network Based Attacks
[Back](../index.md)

-- -

## Netbios and SMB enumeration

NetBIOS is an API and a set of network protocols for providing communication services over a local network. It's used primarily to allow applications on different computers to find and interact with each other on a network.


Functions: NetBIOS offers three primary services:
+ Name Service (NetBIOS-NS): Allows computers to register, unregister, and 
resolve names in a local network.
+ Datagram Service (NetBIOS-DGM): Supports connectionless communication and 
broadcasting.
+ Session Service (NetBIOS-SSN): Supports connection-oriented communication for 
more reliable data transfers.
● Ports: NetBIOS typically uses ports 137 (Name Service), 138 (Datagram 
Service), and 139 (Session Service) over UDP and TCP


SMB is a network file sharing protocol that allows computers on a network to share files, printers, and other resources. It is the primary protocol used in Windows networks for these 
purposes.

Functions: SMB provides features for file and printer sharing, named pipes, and inter-process communication (IPC). It allows users to access files on remote computers as if they were local.

Versions: SMB has several versions:
+ SMB 1.0: The original version, which had security vulnerabilities. It was used with older 
operating systems like Windows XP.
+ SMB 2.0/2.1: Introduced with Windows Vista/Windows Server 2008, offering improved 
performance and security.
+ SMB 3.0+: Introduced with Windows 8/Windows Server 2012, adding features like 
encryption, multichannel support, and improvements for virtualization.

 Ports: SMB generally uses port 445 for direct SMB traffic (bypassing NetBIOS) and port 139 
when operating with NetBIOS.


nbtscan ip_addr_range
nmblookup -A ip_addr

Use socks proxy and autoroute to pivot.

-- -

## SNMP

SNMP (Simple Network Management Protocol) is a widely used protocol for monitoring and managing networked devices, such as routers, switches, printers, servers, and more. 

It allows network administrators to query devices for status information, configure certain settings, and receive alerts or traps when specific events occur.

SNMP is an application layer protocol that typically uses UDP for 
transport. It involves three primary components:
+ SNMP Manager: The system responsible for querying and interacting with 
SNMP agents on networked devices.
+ SNMP Agent: Software running on networked devices that responds to 
SNMP queries and sends traps.
+ Management Information Base (MIB): A hierarchical database that defines 
the structure of data available through SNMP. Each piece of data has a 
unique Object Identifier (OID)

 Versions of SNMP:
+ SNMPv1: The earliest version, using community strings (essentially 
passwords) for authentication.
+ SNMPv2c: An improved version with support for bulk transfers but still 
relying on community strings for authentication.
+ SNMPv3: Introduced security features, including encryption, message 
integrity, and user-based authentication.


Ports:
+ Port 161 (UDP): Used for SNMP queries.
+ Port 162 (UDP): Used for SNMP traps (notifications)

Use snmpwalk tool.

--  -