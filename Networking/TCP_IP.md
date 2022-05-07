# TCP/IP Model
[Back to Networking page](./index.md)

---

## TCP IP
- TCP/IP model is kind of implementation of [OSI_Model](OSI_Model.md)
- Vertical approach
- Services , interface and protocols are not clearly distinguished
- 5 Layers
- Layer 7 to 5 of OSI layer combined into application layer in TCP/IP model.
- Also layer 1 to 2 of OSI layer combined to form network access layer .
- Network layer is also renamed as Internet layer.

---

## TCP/IP Model Diagram

|Layer number|Name|
|:--:|:--:|
|4|Application layer|
|3|Transport layer|
|2|Internet layer|
|1|Host to network layer|

---

## TCP/IP Model Diagram (Hybrid)

|Layer number|Name|
|:--:|:--:|
|5|Application layer|
|4|Transport layer|
|3|Internet layer|
|2|Data link layer|
|1|Physical layer|

---

## Function of each layer

- Application Layer : Layer consists many protocols such as file transfer protocol FTP , web service HTTP & HTTPS and for emails SMTP. Handles translation to binary , compresion & encryption/decryption.Creates , manages & ends session. Authentication is also done here. Tracks received and sent data packerts.

- Transport Layer : DIvided data into segments and keeps track where to send data . Also do flow control means speed at data travels to application. Also handles error controls. Have protocols like TCP & UDP. 

- Internet Layer : Handles transmission. Handles logical addressing , path determination and routing. Data handles in terms of packets. Protocols like IPv4 , IPv6 , ICMPv4 & ICMPv6.

- Data Link Layer : Physical addressing like MAC done here. Also does framing i.e. creating frames.

- Physical Layer :  Handles data conversion such as signal to bits . Determines types of media like light i.e. optical fiber, voltage like cable or signal  like wifi.

---

![TCP/IP](https://www.guru99.com/images/1/093019_0615_TCPIPModelW2.png)

---

### Sources : 
- [TCP/IP Model vidoe youtube](https://www.youtube.com/watch?v=wvPe4Zb0tUA&ab_channel=NesoAcademy)
- [geeksforgeeks page](https://www.geeksforgeeks.org/tcp-ip-model/)