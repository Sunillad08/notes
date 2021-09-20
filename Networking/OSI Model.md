# OSI Model
[Back to Networking page](Networking)
- --
- Open system interconnection model
- 7 Layers
- Developed by ISO
---
#### OSI Model Diagram
|Layer number|Name|
|:--:|:--:|
|7|Application layer|
|6|Presentation layer|
|5|Session layer|
|4|Transport layer|
|3|Network layer|
|2|Data link layer|
|1|Physical layer|
- --
- Application Layer : Layer consists many protocols such as file transfer protocol FTP , web service HTTP & HTTPS and for emails SMTP.

- Presentation Layer : Presentation layer handles translation to binary , compresion & encryption/decryption.
- Session Layer : Creates , manages & ends session. Authentication is also done here. Tracks received and sent data packerts.
- Transport Layer : DIvided data into segments and keeps track where to send data . Also do flow control means speed at data travels to application. Also handles error controls. Have protocols like TCP & UDP. 
- Network Layer : Handles transmission. Handles logical addressing , path determination and routing. Data handles in terms of packets. Protocols like IPv4 , IPv6 , ICMPv4 & ICMPv6.
- Data Link Layer : physical addressing like MAC done here. Also does framing i.e. creating frames.
- Physical Layer :  Handles data conversion such as signal to bits . Determines types of media like light i.e. optical fiber, voltage like cable or signal  like wifi.

![OSI](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2F2.bp.blogspot.com%2F-oL2B7rB_Ddc%2FUXus4JZPgXI%2FAAAAAAAAAKc%2Fe0pDS9JpRD8%2Fs1600%2Fosi.gif&f=1&nofb=1)
- --
#### Sources : 
[OSI Model vidoe youtube](https://www.youtube.com/watch?v=vv4y_uOneC0&ab_channel=TechTerms)
[Wiki Page](https://en.wikipedia.org/wiki/OSI_model)