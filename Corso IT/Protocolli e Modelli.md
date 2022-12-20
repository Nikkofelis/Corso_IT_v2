
```ad-abstract
title: Protocols

Rules that defines how devices communicates.
```

Protocol Examples:

- HTTP: Controls how web client and web server interacts
- TCP: Guaranties the information are delivered
- IP: Delivering messages from sender to receiver
- DNS: Assigns an IP to a site name
- DHCP: Automatically assigns an IP to a device

Overhead: Codice di comunicazione, parte del messaggio usato solo a contenere le informazioni per inviare il messaggio. Da distinguere dal contenuto del messaggio.

# [Network Protocol Requirements](Network%20Protocol%20Requirements.md)

# Network Protocol Functions

| Function                  | Description                                                                                                                                                                                                                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Addressing**            | This ==identifies the sender and the intended receiver== of the message using a defined addressing scheme. Examples of protocols that provide addressing include Ethernet, IPv4, and IPv6.                                                                                          |
| **Reliability**           | This function provides ==guaranteed delivery== mechanisms in case messages are lost or corrupted in transit. TCP provides guaranteed delivery.                                                                                                                                      |
| **Flow control**          | This function ==ensures that data flows at an efficient rate== between two communicating devices. TCP provides flow control services.                                                                                                                                               | 
| **Sequencing**            | This function uniquely ==labels each transmitted segment of data==. The receiving device uses the sequencing information to reassemble the information correctly. This is useful if the data segments are lost, delayed or received out-of-order. TCP provides sequencing services. |
| **Error Detection**       | This function is used to ==determine if data became corrupted during transmission==. Various protocols that provide error detection include Ethernet, IPv4, IPv6, and TCP.                                                                                                          |
| **Application Interface** | This function contains ==information used for process-to-process communications== between network applications. For example, when accessing a web page, HTTP or HTTPS protocols are used to communicate between the client and server web processes.                                |

- Addressing -> Find addresses
- Reliability -> Reliable for delivery
- Flow control -> Efficient flow
- Sequencing -> Message divided
- Error detection -> Finds errors
- Application interface -> How to use data

# [Network Protocol Suites](Network%20Protocol%20Suites.md)

# Protocol Stack Table

The advantages of using a layered model are:

- Assist in protocol design
- Foster competition between vendors
- Prevents a layer to affect another one
- Common language to describe network functionality
- Helps in visualisation of interaction between layers

| OSI Model Layer                                  | Description                                                                                                                                                                            |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [7. Application Layer](Application%20Layer.md)   | Contains protocols used for process-to-process communications.                                                                                                                         |
| [6. Presentation Layer](Presentation%20Layer.md) | Provides for common representation of the data transferred between application layer services.                                                                                         |
| [5. Session Layer](Session%20Layer.md)           | Provides services to the presentation layer to organize its dialogue and to manage data exchange.                                                                                      |
| [4. Transport Layer](Transport%20Layer.md)       | Defines services to segment, transfer, and reassemble the data for individual communications between the end devices.                                                                  |
| [3. Network Layer](Network%20Layer.md)           | Provides services to exchange the individual pieces of data over the network between identified end devices. (Router device)                                                           |
| [2. Data Link Layer](Data%20Link%20Layer.md)     | Describe methods for exchanging data frames between devices over a common media (Switch device)                                                                                        |
| [1. Physical Layer](Physical%20Layer.md)         | Describe the mechanical, electrical, functional, and procedural means to activate, maintain, and de-activate physical connections for a bit transmission to and from a network device. |
^OSI

PhDaNeTSPA

# Data Encapsulation

It moves DOWN on the [Protocol Stack Table](#Protocol%20Stack%20Table).

- **Segmentation**: process of dividing a stream of data into smaller units for transmissions over the network.
- **Multiplexing**: Segmentation done by multiple devices simultaneously.
- **Sequencing**: Labelling of data segments for reassembling.

