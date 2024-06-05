# FTP
[Back to networking page](../index.md)

---

## What is FTP?
**File Transfer Protocol**
The File Transfer Protocol (FTP) is a standard communication protocol used for the transfer of computer files from a server to a client on a computer network. FTP is built on a client–server model architecture using separate control and data connections between the client and the server. 

FTP users may authenticate themselves with a clear-text sign-in protocol, normally in the form of a username and password, but can connect anonymously if the server is configured to allow it. 

For secure transmission that protects the username and password, and encrypts the content, FTP is often secured with SSL/TLS (FTPS) or replaced with SSH File Transfer Protocol [SFTP](FTP.md#SFTP).

Uses TCP.
Port 21 is used for control connection and port 20 is used for data transfer.
Port 20 is only opened when data transfer is going on.

---

## Why it is used?
- To transfer files between computes
- Upload files on server
- Not encrypted , clear text transfer

![FTP](https://images.ctfassets.net/bg6mjhdcqk2h/3kFoQpGfA7LNgm6kG5lq2W/b93b67522195335aec9c5b172d2e6500/Raysync_FTP_Server.png)

---

# SFTP
**Secure File Transfer Protocol**
In computing, the SSH File Transfer Protocol (also Secure File Transfer Protocol, or SFTP) is a network protocol that provides file access, file transfer, and file management over any reliable data stream. It was designed by the Internet Engineering Task Force (IETF) as an extension of the Secure Shell protocol (SSH) version 2.0 to provide secure file transfer capabilities. The IETF Internet Draft states that, even though this protocol is described in the context of the SSH-2 protocol, it could be used in a number of different applications, such as secure file transfer over Transport Layer Security (TLS) and transfer of management information in VPN applications.

This protocol assumes that it is run over a secure channel, such as SSH, that the server has already authenticated the client, and that the identity of the client user is available to the protocol.

Used TCP , part of SSH protocol .

---

# FTPS
FTPS (also known FTP-SSL, and FTP Secure) is an extension to the commonly used File Transfer Protocol (FTP) that adds support for the Transport Layer Security (TLS) and, formerly, the Secure Sockets Layer (SSL, which is now prohibited by RFC7568) cryptographic protocols.

FTPS should not be confused with the SSH File Transfer Protocol (SFTP), a secure file transfer subsystem for the Secure Shell (SSH) protocol with which it is not compatible. It is also different from FTP over SSH, which is the practice of tunneling FTP through an SSH connection.

---

# TFTP
**Trivial FIle Transfer Protocol**
Trivial File Transfer Protocol (TFTP) is a simple lockstep File Transfer Protocol which allows a client to get a file from or put a file onto a remote host. One of its primary uses is in the early stages of nodes booting from a local area network. TFTP has been used for this application because it is very simple to implement.

TFTP was first standardized in 1981 and the current specification for the protocol can be found in RFC 1350.

Just like FTP but uses UDP and mostly use in local areal network . 

---

### Sources
- [FTP wiki](https://en.wikipedia.org/wiki/File_Transfer_Protocol)
- [SFTP wiki](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol)
- [FTPS wiki](https://en.wikipedia.org/wiki/FTPS)
- [TFTP wiki ](https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol)
- [Youtube](https://youtu.be/tOj8MSEIbfA)
- [Youtube](https://youtu.be/L9aZpg0ip70)