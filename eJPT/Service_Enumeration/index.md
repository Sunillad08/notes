# Service Enumeration
[Back](../index.md)

-- -
## FTP

- Try anonymous login : For password press ENTER

- Try Username enumeration using [hydra](../../Cyber_Security/Tools/hydra.md)

- Try Password brute force using [hydra](../../Cyber_Security/Tools/hydra.md) or [nmap](../../Cyber_Security/Tools/nmap.md) FTP Brute script.

Once we get access to files , we can use `get filename` command to get copy of file on our system. 

-- -
## SSH

- Use nmap to gether version of SSH

- Use [Netcat](../../Cyber_Security/Tools/Netcat.md) to connect with SSH port for banner grabbing.

- Use [nmap](../../Cyber_Security/Tools/nmap.md) scripts to enumerate key used by ssh, auth methods allowed for users.

### Dictionary attack - Bruteforce approach

- Use [hydra](../../Cyber_Security/Tools/hydra.md), [nmap](../../Cyber_Security/Tools/nmap.md) or  [Metasploit](../../Cyber_Security/Tools/Metasploit.md) for username enumeration and password brute forcing.

-- -

## HTTP

- Check Robots.txt or sitemap.xml for directory listings.

- Use [dirb](../../Cyber_Security/Tools/dirb.md) , [nmap](../../Cyber_Security/Tools/nmap.md) scripts or [gobuster](../../Cyber_Security/Tools/gobuster.md) for directory enumeration.

- Use wapplyzer extension or whatweb command line tool to identify web technologies used.

- `http URL`  to gather header information

- Use http-enum, http-methods and http-headers nmap scripts to gather information

- Browsh or Lynx tool to render page template on command line.

- Use [Metasploit](../../Cyber_Security/Tools/Metasploit.md) for enumeration of directory , discover available methods. Metasploit modules such as http_version, http_header, robots_txt, dir_scanner, files_dir, http_login can be used to enumerate information.

-- -
## SMB

Port 135 : Remote Procedure Call RPC client server communication 
Port 139 : netbios Network basic input/output system
Port 445 : Server message block SMB

net command on windows
- net use * /delete
- net use Z: \\IP 

Nmap scripts 
smb-protocols , smb-security-mode , smb-enum-sessions, smb-enum-shares , smb-enum-users , smb-server-stats, smb-enum-domains , dmb-enum-groups , smb-enum-services 

msfconsole : smb_version , smb_enumusers , smb_enumshares , smb_login

[smbmap](../../Cyber_Security/Tools/smbmap.md)
Smbmap -H host -u username -p password
--upload
--download

use smbclient to connect to SMB services.

-- -
## SMTP

- [SMTP](../../Networking/Protocols/SMTP.md) runs on port 25 and if [SSL](../../Networking/Protocols/SSL.md) is configured then on 465 or 587.

- Use [Metasploit](../../Cyber_Security/Tools/Metasploit.md) modules such as smtp_enum and smtp_version to gather information.

- We can also use ```smtp-enum-user``` command to enumerate users. We can also use ```sendemail``` to send emails.

- Connect to SMTP port and Use VRFY command to find if user actually exists or not. 

- Use [Command List](https://mailtrap.io/blog/smtp-commands-and-responses/) to run desired commands.

-- -

## MySQL

- Generally hosted on port 3306

- Metasploit Modules
	- mysql_version: version
	- mysql_login login bruteforce
	- mysql_enum: enumerate users
	- mysql_sql: interact with sql server
	- mysql_schemadump: Dump schema structure of database

- Use cmd: mysql ip -u username -P

-- -


