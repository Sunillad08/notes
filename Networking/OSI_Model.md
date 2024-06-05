# OSI Model
[Back to Networking page](./index.md)

---

The OSI model is composed of seven ordered layers: physical (layer 1), data link (layer 2), network (layer 3), transport (layer 4), session (layer 5), presentation (layer 6),
and application (layer 7).

- Open system interconnection model
- 7 Layers
- Developed by ISO

---

## OSI Model Diagram

|Layer number|Name|
|:----------:|:--:|
|7|Application layer|
|6|Presentation layer|
|5|Session layer|
|4|Transport layer|
|3|Network layer|
|2|Data link layer|
|1|Physical layer|

---

 ## Basic working
 
- Application Layer : Layer consists many protocols such as file transfer protocol FTP , web service HTTP & HTTPS and for emails SMTP.

- Presentation Layer : Presentation layer handles translation to binary , compresion & encryption/decryption.

- Session Layer : Creates , manages & ends session. Authentication is also done here. Tracks received and sent data packerts.

- Transport Layer : DIvided data into segments and keeps track where to send data . Also do flow control means speed at data travels to application. Also handles error controls. Have protocols like TCP & UDP. 

- Network Layer : Handles transmission. Handles logical addressing , path determination and routing. Data handles in terms of packets. Protocols like IPv4 , IPv6 , ICMPv4 & ICMPv6.

- Data Link Layer : physical addressing like MAC done here. Also does framing i.e. creating frames.

- Physical Layer :  Handles data conversion such as signal to bits . Determines types of media like light i.e. optical fiber, voltage like cable or signal  like wifi.

---

## Function

### Application Layer
- Network Virtual Terminal : To allow remote user to get software version of physical terminal
- File transfer , access and management : To access files in a remote host , change or update file on system
- Email : Email forwarding and storage
- Directory services : Distributed database sources and access gloabal information

### Presentation Layer
- Translation : Converts information so system can understand it.
- Encryption : Encryptes outgoing traffic and decryptes incoming data
- Compression : Compression and decompression of data for efficient data transfer.

### Session Layer 
- Dialog control : Allows two processes to take place either in half duplex or full duplex mode.
- Synchronization : Adds checkpoints into stream of data for control flow.

### Transport Layer
- Service-point addressing : Identifies and differentiate services using [Ports](Ports.md) . 
- Segmentation and reassembly : Messages are divided into segments for transmission and reassembled upon arriving.
- Connection control : Connectionless or connection-oriented services for better transmission policy.
- Flow control : To control flow of data for end to end transmission.
- Error control : To avoid errors and cover up errors if it happens.

### Network Layer
- Logical Addressing : Logical addressing using [IP](Protocols/IP.md) to distinguish multiple devices on internet.
- Routing : Transfer of packets from one device to other.

### Data link Layer
- Framing : Divide packets into frames for manageable data units.
- Physical addressing : Physical addressing using [MAC](Protocols/MAC.md) address.
- Flow control : Control flow of data transfer
- Access control : Determine access to link for two or more devices.
- Error control : Add trailer to achieve error control.

### Physical Layer
- Physical characteristics : Defines transmission media
- Representation of bits : Bit length and encoding
- Data rate and synchronization : Synchronize data transfer and manage data rate
- Physical topology : Topology
- Transmission mode : Either simplex , half duplex or duplex

---

![OSI](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F2.bp.blogspot.com%2F-oL2B7rB_Ddc%2FUXus4JZPgXI%2FAAAAAAAAAKc%2Fe0pDS9JpRD8%2Fs1600%2Fosi.gif&f=1&nofb=1)

![Detailed OSI](https://media.fs.com/images/community/upload/kindEditor/202107/29/original-seven-layers-of-osi-model-1627523878-JYjV8oybcC.png)

---

### Sources : 
- [OSI Model vidoe youtube](https://youtu.be/vv4y_uOneC0)
- [Wiki Page](https://en.wikipedia.org/wiki/OSI_model)
- [OSI Model Youtube Hindi](https://youtu.be/UvHr0yL-wJg)