# Service Enumeration
[Back](../index.md)

-- -
Quick Access

- [FTP](#FTP)

-- -
# FTP

- Try anonymous login : For password press ENTER

- Try Username enumeration using [hydra](../../Cyber_Security/Tools/hydra.md)

- Try Password brute force using [hydra](../../Cyber_Security/Tools/hydra.md) or [nmap](../../Cyber_Security/Tools/nmap.md) FTP Brute script.

Once we get access to files , we can use `get filename` command to get copy of file on our system. 

-- -
# SSH

- Use nmap to gether version of SSH

- Use [Netcat](../../Cyber_Security/Tools/Netcat.md) to connect with SSH port for banner grabbing.

- Use [nmap](../../Cyber_Security/Tools/nmap.md) scripts to enumerate key used by ssh, auth methods allowed for users.

## Dictionary attack - Bruteforce approach

- Use [hydra](../../Cyber_Security/Tools/hydra.md), [nmap](../../Cyber_Security/Tools/nmap.md) or  [Metasploit](../../Cyber_Security/Tools/Metasploit.md) for username enumeration and password brute forcing.

-- -