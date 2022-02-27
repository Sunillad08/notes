# Frames
[Back to networking page](index.md)
- --
## What are frames?
A frame is a digital data transmission unit in computer networking and telecommunication. In packet switched systems, a frame is a simple container for a single network packet. In other telecommunications systems, a frame is a repeating structure supporting time-division multiplexing.

In the [OSI_Model](OSI_Model.md)  of computer networking, a frame is the protocol data unit at the data link layer. Even in [TCP_IP](TCP_IP.md) .
- --
## Why we use frame?
A frame typically includes frame synchronization features consisting of a sequence of bits or symbols that indicate to the receiver the beginning and end of the payload data within the stream of symbols or bits it receives. If a receiver is connected to the system during frame transmission, it ignores the data until it detects a new frame synchronization sequence.
- --
## Diagram
![Diagram|700](https://techdifferences.com/wp-content/uploads/2017/08/featured-4.jpg)

![Headers|700](https://www.ionos.com/digitalguide/fileadmin/DigitalGuide/Screenshots_2018/EN-ethernet-frame-structure5.jpg)

Headers change as per frame types. This is ethernet frame headers.

-  Preamble , SFD : 7 bytes info that says frame is coming and where frame starts to NIC.
-  Destination MAC address : MAC address of receiver(Next node to transfer).
-  Source MAX address : MAC address of sender(Changes as per node to node)
-  Length : Length of data
-  Data : payload or IP packet (Atleast 46 bytes)
-  Frame check sequence : Error checking mechanism.

- --
### Source 
- [Wiki](https://en.wikipedia.org/wiki/Frame_(networking))
- [Short video](https://youtu.be/qXtS1o1HGso)
- [Detailed video](https://youtu.be/ewpq3qxx5Ls)