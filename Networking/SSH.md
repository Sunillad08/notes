# SSH
[Back to networking page](./index.md)

---

## What is SSH?
**Secure Shell**
Secure Shell (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network. Typical applications include remote command-line, login, and remote command execution, but any network service can be secured with SSH.

Port 22 is used.

---

## Why SSH is used?
SSH provides a secure channel over an unsecured network by using a client–server architecture, connecting an SSH client application with an SSH server. The protocol specification distinguishes between two major versions, referred to as SSH-1 and SSH-2. The standard TCP port for SSH is 22. SSH is generally used to access Unix-like operating systems, but it can also be used on Microsoft Windows. Windows 10 uses OpenSSH as its default SSH client and SSH server.

---

## SSH Components
1. **SSH-Trans** : SSH-Trans is software that implements security over insecure TCP channel. In this phase , they exchange many security parameters and establish secure channel on top of TCP. Server authentication is done here. Compression of message is also done here to improve efficiency.
2. **SSH-AUTH** : SSH-AUTH authenticates client and server. SSH calls another software that can authenticate client for server. 
3. **SSH-CONN** : SSH-CONN do multiplexing on already established channel. It creates multiple logical channels over it.
4. **SSH Applications** : After connection phase is completed , SSH allows several programs to use the connection. 

---

## SSH Tunneling 
SSH tunneling or port forwarding is service provided by ssh to other protocols so they can use secure tunnel. 

---

## SSH Packet format

![ssh packet format](https://images.slideplayer.com/26/8842511/slides/slide_34.jpg)

---
## About SSH
SSH was designed as a replacement for [Telnet](Telnet.md) and for unsecured remote shell protocols such as the Berkeley rsh and the related rlogin and rexec protocols. Those protocols send sensitive information, notably passwords, in plaintext, rendering them susceptible to interception and disclosure using packet analysis. The encryption used by SSH is intended to provide confidentiality and integrity of data over an unsecured network, such as the Internet.

---

## How to setup SSH?
On Linux

```bash
sudo apt-get install openssh-server
systemctl status enable sshd # to check if running or not
systemctl start start sshd # start / enable depending of version
```

---

## Sources :
- [Wiki](https://en.wikipedia.org/wiki/Secure_Shell)
- [Youtube](https://youtu.be/qWKK_PNHnnA)
- [ssh](https://www.youtube.com/watch?v=tZop-zjYkrU&ab_channel=PowerCertAnimatedVideos)
- [Configure ssh](https://youtu.be/1hvVcEhcbLM?t=11100)
- [How ssh work](https://youtu.be/ORcvSkgdA58)