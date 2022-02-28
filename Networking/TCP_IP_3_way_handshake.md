## TCP 3 way handshake
[Back to Networking page](./index.md)

---

- [TCP](TCP.md) connection is done through 3 way handshake process
- 3 way handshake establishes connection.

### Diagram
![3-way-handshake](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flh4.googleusercontent.com%2Fproxy%2FihfN3Ow6OiqDnjWx6psWkcGinOJZ4ErkrgjP7wBoBJXYYPcdoqIpZEBbdpgMIeS-mGeZnUv5V8YZ3s6thFS_2uQud1wV9KAPzTQblT-IHPLsHwHjlfEd0FQYp6QugR9VSvwmjorKDEKFa5c7qnAloCctIf6xBUNVLK0SREI905tBW48Xliglzk4MIA%3Dw1200-h630-p-k-no-nu&f=1&nofb=1)

![3-way-handshake](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.tcpipguide.com%2Ffree%2Fdiagrams%2Ftcpopen3way.png&f=1&nofb=1)

### Explanation
- Client sends SYN message to initiate connection. Also sends seq number
- Server sends SYN+ACK message with seq number & Ack number which is client seq number + 1 .
- Client sends ACK message with client seq+1 and Ack number which is server seq number + 1.
- If server replies with RST & ACK flag then port status is closed.
- --
### Sources :
- [Youtube video - short](https://www.youtube.com/watch?v=xMtP5ZB3wSk&ab_channel=SunnyClassroom)
- [Youtube video - detailed](https://www.youtube.com/watch?v=qIEHUUt2Wfc&ab_channel=GateSmashers)
- [Detailed Hindi video](https://youtu.be/s9FDHiCb2nk)
- [Website](https://www.guru99.com/tcp-3-way-handshake.html)