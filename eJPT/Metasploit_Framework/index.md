# Metasploit Framework
[Back](../index.md)

-- -

## Metasploit Framework (MSF)

The Metasploit Framework (MSF) is an open-source, robust penetration testing and exploitation framework that is used by penetration testers and security researchers worldwide.

Essential Terminology
+ Interface – Methods of interacting with the Metasploit Framework.
+ Module – Pieces of code that perform a particular task, an example of a module is an 
exploit.
+ Vulnerability – Weakness or flaw in a computer system or network that can be exploited.
+ Exploit – Piece of code/module that is used to take advantage a vulnerability within a 
system, service or application.
+ Payload – Piece of code delivered to the target system by an exploit with the objective of 
executing arbitrary commands or providing remote access to an attacker.
+ Listener – A utility that listens for an incoming connection from a target.

-- -

## Metasploit Framework Architecture

![test](https://www.offsec.com/app/uploads/2015/04/msfarch2.png)


### MSF Modules


- Exploit - A module that is used to take advantage of vulnerability and is typically paired with a payload.

- Payload - Code that is delivered by MSF and remotely executed on the target after successful xploitation. An example of a payload is a reverse shell that initiates a connection from the target system back to the attacker.

- Encoder - Used to encode payloads in order to avoid AV detection. For example, shikata_ga_nai is used to encode Windows payloads.

- NOPS - Used to ensure that payloads sizes are consistent and ensure the stability of a payload when executed.

- Auxiliary - A module that is used to perform additional functionality like port scanning and enumeration.

-- -

### MSF Payload Types
- Unstaged : Payload is sent to system along with exploits

- Staged : A staged payload is sent.
The first part (stager) contains a payload that is used to establish a reverse connection back to the attacker, download the second part of the payload (stage) and execute it.
    - Stagers : Establish stable communication.
    - Stage : Payload component downloaded by stagers.

The Meterpreter (Meta-Interpreter) payload is an advanced multi-functional payload that is executed in memory on the target system making it difficult to detect.It communicates over a stager socket and provides an attacker with an interactive command interpreter on the target system that facilitates the execution of system commands, file system navigation, keylogging and much more.

+ MSF stores modules under the following directory on Linux systems: /usr/share/metasploit-framework/modules
+ User specified modules are stored under the following directory on Linux systems: ~/.ms4/modules

-- -

## Setup and Configuration

- Install metasploit-framework
- Start postgresql service
- Initialize msfdb
- Use msfconsole command

## msfconsole Fundamentals

- LHOST , LPORT are set attacker IP and Port Number.
- RHOST/RHOSTS , RPORT are set to victim's IP/IPs and Port Number.
- Use search to find modules , use to use modules, set to set value, unset to remove value , run or exploit to run module.

-- -

## Workspaces

Workspaces allow you to keep track of all your osts, scans and activities and are extremely useful when conducting penetration tests as they allow you to sort and organize your data based on the target or organization.

Usage: 
- workspace : List workspaces
- workspace -a name : Add workspace
- workspace -d name : delete workspace
- workspace name : Switch workspace
- workspace -r old new : Rename workspace

-- -

## Import nmap result into msfconsole
Do nmap scan and store output in XML format.Create a workspace. Import results using ```db_import nmap_xml_result``` command.

**OR**

Use db_nmap to perform nmap scan.

hosts : Host in nmap results
services : Services discoverd
vulns : Find vulnerabilities

-- -

## Route traffic through machine

Run following command on meterpreter session.
```run autoroute -s IP_to_route_through```

## Information gathering

FTP
- ftp_version : Enumerate version
- ftp_login : Bruteforce credentials
- anonymous : Verify if anonymous login is allowed

SSH 
- ssh_version : Enumerate version
- ssh_login : Bruteforce credentials
- ssh_enumusers : Enumerate users

SMB
- smb_version : Enumerate version
- smb_enumusers : Enumerate users
- smb_enumshares : Enumerate shares
- smb_login : Bruteforce credentials

SMTP
- smtp_version : Enumerate version
- smtp_enum : Enumerate users

HTTP
- http_version : Enumerate version
- http_header : Get header information
- robots_txt : robots.txt file
- dir_scanner : Directory enumeration
- files_dir : Files enumeration
- http_login : Bruteforce credentials

MySql
- mysql_version : Enumerate version
- mysql_login : Credentials bruteforce
- mysql_enum : Enumerate users
- mysql_sq l: Interact with sql server
- mysql_schemadump : Dump schema structure of database

-- -
