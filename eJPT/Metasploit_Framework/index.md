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

## msfvenom

Generating msfvenom payload

msfvenom --list payloads : To list all payloads
msfvenom --list format : To list all formats of payload

Staged payload : /meterpreter/type
Unstaged payload : /meterpreter_type

-p : payload path
LHOST : Attacker IP
LPORT : Attacker Port
-f : file type like exe
-a : architecture

-e : encoder (-e x86/shikata_ga_nai)
-i : iterations of encoding

-x : inject payload in actual software and replace it to exploit
-k : keep original functionality of software plus exploit


-- -

## meterpreter session basic

sessions : Show all ongoing sessions
(
    -C : Run meterpreter command on any session
    -l : list active session
    -k : kill session
    -n : name session
    -i : id of session
)

sysinfo : System Information
getuid : user permission and level
download : download file
upload : upload file
checksum md5 : MD5 checksum
getenv PATH : get environment path
search : search for file 
(
    -f : file extension
    -d : directory to search in
)
shell : native session
ps : process list
migrate _id_ : migrate to process
execute -f command : execute command on machine

-- -

## Upgrade shell to meterpreter

use multi/manage/shell_to_meterpreter to upgrade 
use sessions -u  _id_


-- -

## Windows POST


- getsystem : Upgrade user privilege
- show_mount : Show mounted devices
- hashdump : Dump hashes
- pgrep name : Get PID of process
- migrate : migrate to other service

post/windows/manage/migrate : migrate to other service
post/windows/manage/archmigrate : migrate architecture

windows/gather/win_privs : Gather user windows privilege
windows/gather/enum_logged_on_users  : Gather information regarding logged in users
windows/gather/checkvm : Check if machine is Virtual machine
windows/gather/enum_applications : Enumerate installed application versions
windows/gather/enum_av_excluded : Excluded folders from antivirus scan
windows/gather/enum_computers : Enumerate computers included in AD Domain.
windows/gather/enum_patches : Enumerate patches installed on system
windows/gather/enum_shares : Enumerate shares target is part of


### UAC bypass

windows/local/bypassuac_injection : UAC bypass (Match architecture for payloads)


### Persistence on windows 

windows/local/persistence_service : Add persistence via service

windows/manage/enable_rdp : Enable RDP on system
Use ```net user user password``` for adding password to users.
Use xfreerdp /u:username /p:password /v:host to connect to RDP. 

### Keylogging
Get meterpreter session 
keyscan_start : Start key logging
keyscan_dump : Dump captured key_stroke
keyscan_stop : Stop keylogging

### Windows logs clearing

Logs can be accessed from Event Viewer
We require elevated privilege for clearing logs
Use clearev in meterpreter command to clear logs


-- -

## Linux Post Exploitation Modules

Modules use to gather information post exploitation phase.

- post/linux/gather/enum_configs : Enumerate config files such as sshd
- post/multi/gather/env : Get Environment variables
- post/linux/gather/enum_network : Enumerate Network details
- post/linux/gather/enum_protections : Enumerate system hardening mechanisms
- post/linux/gather/enum_system : Enumerate system information like cronjobs
- post/linux/gather/checkcontainer : Check if system is running in container
- post/linux/gather/checkvm : Check if system in running in Virtual Environment
- post/linux/gather/enum_users_history : Enumerate User history stored in command history files
- post/multi/manage/system_session : Create Reverse TCP shell with environment already present on system.
- post/linux/manage/download_exec : Download and run file with bash.


### Exploiting vulnerable program

ps aux to find running services
check if any service is vulnerable 

exploit/unix/local/chkrootkit : To get root privilege 


### Hashdump

- post/multi/gather/ssh_creds : Gather SSH credentials from .ssh directory
- post/multi/gather/docker_creds : Gather cred from .docker directory
- post/linux/gather/hashdump :  Dump hashes from system
- post/linux/gather/ecryptfs_creds : Gather cred from .ecrypts directories
- post/linux/gather/enum_psk : Gather wireless security credentials
- post/linux/gather/enum_hexchat : Gather cred from hexchat and xchat config files
- post/linux/gather/phpmyadmin_credsteal : Gather phpmyadmin cred 
- post/linux/gather/pptpd_chap_secrets : Gather PPT VPN information
- post/linux/manage/sshkey_persistence :  Add SSH key to user for remote login


### Establishing Persistence On Linux

Persistence consists of techniques that adversaries use to keep access to systems across restarts, changed credentials, and other interruptions that could cut off their access.

Add user on system having root privilege and name of service account such as ftp.
useradd -m username -s shell
passwd username
usermod -aG root username
usermod -u user_id username


linux/local/cron_persistence : Manipulate cronjob for persistence
exploit/linux/local/service_persistence : Add persistence via service
post/linux/manage/sshkey_persistence : Add SSH key for persistence 

-- -

## Pivoting

Pivoting is a post exploitation technique that involves utilizing a compromised host to attack other systems on the compromised host’s private internal network.

run autoroute -s ip_subnet

port forwarding via meterpreter session
portfwd add -l local_port -p pivot_port -r  pivot_machine

While running attack on pivot machine,
Change payload to bind payload and set LHOST to machine we have exploited.

-- -

## Armitage

GUI version of msfconsole

