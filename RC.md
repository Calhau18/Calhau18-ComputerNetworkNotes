# Chapter 1: Computer Networks and the Internet

## What Is the Internet?

The **Internet** is a computer network that interconnects billions of computing devices throughout the world.
When one **end system** has data to send to another end system, the sending end system segments the data and adds header bytes to each segment. The resulting packages of information, known as **packets** in the jargon of computer networks, are then sent through the network to the destination end system, where they are reassembled into the original data. A packet switch takes a packet arriving on one of its incoming communication the original data.
A packet switch takes a packet arriving on one of its incoming communication
links and forwards that packet on one of its outgoing communication links. Packet switches come in many shapes and flavors, but the two most prominent types in today’s Internet are **routers** and **link-layer** switches.
The sequence of communication links and packet switches traversed by a packet from the sending end system to the receiving end system is known as a **route** or **path** through the network.

End systems access the Internet through **Internet Service Providers (ISPs)**. The Internet is all about connecting end systems to each other, so the ISPs that provide access to end systems must also be interconnected. These lower- tier ISPs are thus interconnected through national and international upper-tier ISPs and these upper-tier ISPs are connected directly to each other. An upper-tier ISP consists of high-speed routers interconnected with high-speed fiber-optic links.

End systems, packet switches, and other pieces of the Internet run **protocols** that control the sending and receiving of information within the Internet. The **Transmission Control Protocol (TCP)** and the **Internet Protocol (IP)** are two of the most impor- tant protocols in the Internet. The IP protocol specifies the format of the packets that are sent and received among routers and end systems. The Internet’s principal protocols are collectively known as **TCP/IP**.

**Protocol (definition)**: A protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event.

End systems attached to the Internet provide a **socket interface** that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system.

## The Network Edge

### Access Network

**Access network**: the network that connects an end system to the first router (also known as the "edge router").

- **Home Access**: DSL, Cable, FTTH, and 5G Fixed Wireless

  - **Digital Subscriber Line (DSL)**

    A residence typically obtains DSL Internet access from the same local telephone company that provides its wired local phone access. The home's DSL modem takes digital data and translates it to high-frequency tones for transmission over telephone wires to the **central office (CO)** of the telephone company (telco). The residential telephone line carries both data and traditional telephone signals simultaneously, which are encoded at different frequencies:

      - A high-speed downstream channel, in the 50 kHz to 1 MHz band
      - A medium-speed upstream channel, in the 4 kHz to 50 kHz band
      - An ordinary two-way telephone channel, in the 0 to 4 kHz band

    At the CO, the analog signals are translated back into digital format at the Digital Subscriber Line Access Multiplexer (DSLAM), and sent into the Internet.

    The DSL standards define multiple transmission rates, namely downstream and upstream. These are actually different, which leads us to call the access **asymmetric**.
    The maximum rates are limited by the distance between the home and the CO.

  - **Cable**

    Cable Internet access makes use of the cable television company’s existing cable television infrastructure.
    Fiber optics connect the cable head end to neighborhood-level junctions, from which traditional coaxial cable is then used to reach individual houses. Because both fiber and coaxial cable are employed in this system, it is often referred to as **hybrid fiber coax (HFC)**.

    Cable internet access requires special modems, called **cable modems**. As with a DSL modem, the cable modem is typically an external device and connects to the home PC through an Ethernet port. 
    At the cable head end, the **cable modem termination system (CMTS)** serves a similar function as the DSL network’s DSLAM, turning the analog signal sent from the cable modems in many downstream homes back into digital format.
    Cable modems divide the HFC network into two channels, a downstream and an upstream channel. As with DSL, access is typically asymmetric, with the downstream channel typically allocated a higher transmission rate than the upstream channel.

    One important characteristic of cable Internet access is that it is a shared broadcast medium. In particular, every packet sent by the head end travels downstream on every link to every home and every packet sent by a home travels on the upstream channel to the head end. For this reason, if several users are simultaneously downloading a video file on the downstream channel, the actual rate at which each user receives its video file will be significantly lower than the aggregate cable downstream rate. On the other hand, if there are only a few active users and they are all Web surfing, then each of the users may actually receive Web pages at the full cable downstream rate, because the users will rarely request a Web page at exactly the same time. Because the upstream channel is also shared, a distributed multiple access

  - **Fiber To The Home (FTTH)**

    FTTH is an up-and-coming technology that provides even higher speed than the aforementioned methods. 
    The concept is simple - provide an optical fiber paht from the CO directly to the home. FTTH can potentially provide Internet access rates in the gigabits per second range.
    The simplest optical distribution network is called direct fiber, with one fiber leaving the CO for each home. More commonly, each fiber leaving the central office is actually shared by many homes; it is not until the fiber gets relatively close to the homes that it is split into individual customer-specific fibers.

  - **5G fixed wireless**
    
    5G fixed wireless is beginning to be deployed and promises high-speed residential access, but will do so without installing costly and failur-prone abling from the telco's CO to the home. 
    With 5G fixed wireless, using beam-forming technology, data is sent wirelessly from a provider’s base station to the a modem in the home. A WiFi wireless router is connected to the modem, similar to how a WiFi wireless router is connected to a cable or DSL modem.

- **Enterprise (and Home) Access**: Ethernet and WiFi

  On corporate and university campuses, and increasingly in home settings, a **local area network (LAN)** is used to connect an end system to the edge router. Although there are many types of LAN technologies, Ethernet is by far the most prevalent access technology in corporate, university, and home networks. As shown in
  Ethernet users use twisted-pair copper wire to connect to an Ethernet switch. The Ethernet switch, or a network of such interconnected switches, is then in turn connected into the larger Internet.
  In a wireless LAN setting, wireless users transmit/receive packets to/from an **access point** that is connected into the enterprise’s network.
  Wireless LAN access based on IEEE 802.11 technology, more colloquially known as WiFi, is now just about everywhere.

- **Wide-Area Wireless Access**: 3G and LTE 4G and 5G

  Mobile devices employ the same wireless infrastructure used for cellular telephony to send/receive packets through a base station that is operated by a cellular network provider. Unlike WiFi, a user need only be within a few tens of kilometers (as opposed to a few tens of meters) of the base station.
  Telecommunications companies have made enormous investments in so-called fourth-generation (4G) wireless, which provides real-world download speeds of up to 60 Mbps. But even higher-speed wide-area access technologies — a fifth-generation (5G) of wide-area wireless networks—are already being deployed.

### Physical Media

Physical media fall into two categories: **guided/wired media** - waves are guided along a solid medium - and **unguided/wireless media** - waves propagate in the atmosphere and in outer space.

- **Twisted-Pair Copper Wire**

  The least expensive and most commonly used guided transmission medium is twisted-pair copper wire.
  Twisted pair consists of two insulated copper wires, each about 1mm thick, arranged in a regular spin pattern.
  Typically, a number of pairs are bundled together in a cable by wrapping the pairs in a protective shield. 
  A wire pair constitutes a single communication link. 

- **Coaxial Cable**

  Like twisted pair, coaxial cable consists of two copper conductors, but the two conductors are concentric rather than parallel. With this construction and special insulation and shielding, coaxial cable can achieve high data transmission rates.

- **Fiber Optics**

  An optical fiber is a thin, flexible medium that conducts pulses of light, with each pulse representing a bit. A single optical fiber can support tremendous bit rates, up to tens or even hundreds of gigabits per second. 
  They are immune to electromagnetic interference, have very low signal attenuation up to 100 kilometers, and are very hard to tap. 

  These characteristics have made fiber optics the preferred long-haul guided transmission media, particularly for overseas links.
  However, the high cost of optical devices has hindered their deployment for short-haul transport, such as in a LAN or into the home in a residential access network.

- **Terrestrial Radio Channels**

  Radio channels carry signals in the electromagnetic spectrum. They are an attractive medium because they require no physical wire to be installed, can penetrate walls, provide connectivity to a mobile user, and can potentially carry a signal for long distances. The characteristics of a radio channel depend significantly on the propagation environment and the distance over which a signal is to be carried.
   Environmental considerations determine path loss and shadow fading, multipath fading, and interference.
   Terrestrial radio channels can be broadly classified into three groups:

   - those that operate over very short distance (for example with one or two meters): personal devices such as wireless headsets, keyboards, and medical devices operate over short distances;
   - those that operate in local areas, typically spanning from ten to a few hundred meters: wireless LAN technologies;
   - those that operate in the wide area, spanning tens of kilometers: cellular access technologies.  

- **Satellite Radio Channels**

  A communication satellite links two or more Earth-based microwave transmitter/receivers, known as ground stations. Two types of satellites are used in communications: **geostationary satellites (GEO)** and **low-earth orbiting (LEO)** satellites. 

  Geostationary satellites permanently remain above the same spot on Earth. This stationary presence is achieved by placing the satellite in orbit at 36,000 kilometers above Earth’s surface. This huge distance from ground station through satellite back to ground station introduces a substantial signal propagation delay of 280 milliseconds. Nevertheless, satellite links are often used in areas without access to DSL or cable-based Internet access.
  
  LEO satellites are placed much closer to Earth. They rotate around Earth and may communicate with each other, as well as with ground stations. To provide continuous coverage to an area, many satellites need to be placed in orbit. 

## The Network Core

Between source and destination, each packet travels through communication links and **packet switches** (either **routers** or **link-layer switches**).
Packets are transmitted over each communication link at a rate equal to the full transmission rate of the link. So, if a source end system or a packet switch is sending a packet of $L$ bits over a link with transmission rate $R$ bits/sec, then the time to transmit the packet is $L/R$ seconds.

### Packet Switching

#### Store-and-Forward Transmission

Most packet switches use store-and-forward transmission at the inputs to the links. Store-and-forward transmission means that the packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link.

The end-to-end delay of sending $P$ packets of $L$ bytes over a path consisting of $N$ links each of rate $R$ is

$$
(N+P-1) \frac{L}{R}
$$

#### Queuing Delays and Packet Loss

Each packet switch has multiple links attached to it. For each attached link, the packet switch has an output buffer (also called an output queue), which stores packets that the router is about to send into that link.
The output buffers play a key role in packet switching.
If an arriving packet needs to be transmitted onto a link but finds the link busy with the transmission of another packet, the arriving packet must wait in the output buffer.
Thus, in addition to the store-and-forward delays, packets suffer output buffer queuing delays.
These delays are variable and depend on the level of congestion in the network.
Since the amount of buffer space is finite, an arriving packet may find that the buffer is completely full with other packets waiting for transmission.
In this case, **packet loss** will occur — either the arriving packet or one of the already-queued packets will be dropped.

#### Forwarding Tables and Routing Protocols

In the Internet, every end system has an address called an IP address.
When a source end system wants to send a packet to a destination end system, the source includes the destination’s IP address in the packet’s header.
As with postal addresses, this address has a hierarchical structure.
When a packet arrives at a router in the network, the router examines a portion of the packet’s destination address and forwards the packet to an adjacent router.
More specifically, each router has a **forwarding table** that maps destination addresses (or portions of the destination addresses) to that router’s outbound links.
When a packet arrives at a router, the router examines the address and searches its forwarding table, using this destination address, to find the appropriate outbound link.
The router then directs the packet to this outbound link.

### Circuit Switching

In circuit-switched networks, the resources needed along a path (buffers, link transmission rate) to provide for communication between the end systems are reserved for the duration of the communication session between the end systems.

#### Multiplexing in Circuit-Switched Networks

A circuit in a link is implemented with either **frequency-division multiplexing (FDM)** or **time-division multiplexing (TDM)**.

With FDM, the frequency spectrum of a link is divided up among the connections established across the link.
Specifically, the link dedicates a frequency band to each connection for the duration of the connection.
The width of the band is called **bandwidth**.

For a TDM link, time is divided into frames of fixed duration, and each frame is divided into a fixed number of time slots. When the network establishes a connection across a link, the network dedicates one time slot in every frame to this connection. These slots are dedicated for the sole use of that connection, with one time slot available for use (in every frame) to transmit the connection's data.

### Packet vs Circuit Switching

Critics of packet switching have often argued that packet switching is not suitable for real-time services (for example, telephone calls and video conference calls) because of its variable and unpredictable end-to-end delays (due primarily to variable for real-time services because of its variable and unpredictable end-to-end delays.

Proponents of packet switching argue that (1) it offers better sharing of transmission capacity than circuit switching and (2) it is simpler, more efficient, and less costly to implement than circuit switching.

Critics of circuit switching have always argued that circuit switching is wasteful because the dedicated circuits are idle during **silent periods**. 

### A Network of Networks

We saw earlier that end systems connect into the Internet via an access ISP.
The access ISP can provide either wired or wireless connectivity, using an array of access technologies including DSL, cable, FTTH, Wi-Fi, and cellular.
But connecting end users and content providers into an access ISP is only a small piece of solving the puzzle of connecting the billions of end systems that make up the Internet.
To complete this puzzle, the access ISPs themselves must be interconnected.
This is done by creating a network of networks — understanding this phrase is the key to understanding the Internet.

*insert description of network of networks*

## Performance Metrics

### Delay in Packet Switched Networks

In this section we'll analyse the various types of delay associated with the transmission of a packet from the time it reaches a router to the time it reaches the following one.

- **Processing Delay**

  The time required to examine the packet’s header and determine where to direct the packet is part of the processing delay. The processing delay can also include other factors, such as the time needed to check for bit-level errors in the packet that occurred in transmitting the packet’s bits from the upstream node to router the router.

- **Queuing Delay**

  At the queue, the packet experiences a queuing delay as it waits to be transmitted onto the link. The length of the queuing delay of a specific packet will depend on the number of earlier-arriving packets that are queued and waiting for transmission onto the link. If the queue is empty and no other packet is currently being transmitted, then our packet’s queuing delay will be zero. On the other hand, if the traffic is heavy and many other packets are also waiting to be transmitted, the queuing delay will be long.

- **Transmission Delay**

  Assuming that packets are transmitted in a first-come-first-served manner, as is common in packet-switched networks, our packet can be transmitted only after all the packets that have arrived before it have been transmitted. This is the amount of time required to push (that is, transmit) all of the packet’s bits into the link. 

- **Propagation Delay**

  Once a bit is pushed into the link, it needs to propagate to the next router. The bit propagates at the propagation speed of the link, which depends on the physical medium of the link.

### Queuing Delay and Packet Loss

Let $a$ denote the average rate at which packets arrive at the queue ($a$ is in units of packets/sec).
With transmission rate $R$ (in bits/sec) and all packets having $L$ bits, we have that the average rate at which bits arrive at the queue is $La$ bits/sec.
Finally, assume that the queue is very big, so that it can hold essentially an infinite number of bits.
The ratio $\frac{La}{R}$, called the **traffic intensity**, often plays an important role in estimating the extent of the queuing delay.
If $\frac{La}{R} > 1$, then the average rate at which bits arrive at the queue exceeds the rate at which the bits can be transmitted from the queue.
In this unfortunate situation, the queue will tend to increase without bound and the queuing delay will approach infinity!
Therefore, one of the golden rules in traffic engineering is: Design your system so that the traffic intensity is no greater than 1.

Now consider the case $La/R \leq 1$.
Here, the nature of the arriving traffic impacts the queuing delay.
For example, if packets arrive periodically (that is, one packet arrives every $L/R$ seconds) then every packet will arrive at an empty queue and there will be no queuing delay.
On the other hand, if packets arrive in bursts but periodically, there can be a significant average queuing delay.
For example, suppose $N$ packets arrive simultaneously every $\frac{L}{R}N$ seconds.
Then the first packet transmitted has no queuing delay, the second packet transmitted has a queuing delay of $\frac{L}{R}$ seconds and, more generally, the $n$th packet has a queuing delay of $(n-1)\frac{L}{R}$.
This leads to an average delay of $\frac{(N-1)N}{2}\frac{L}{R}$.

The two examples of periodic arrivals described above are a bit academic.
Typically, the arrival process to a queue is random; that is, the arrivals do not follow any pattern and the packets are spaced apart by random amounts of time.
In this more realistic case, the quantity La/R is not usually sufficient to fully characterize the queuing delay statistics.
Nonetheless, it is useful in gaining an intuitive understanding of the extent of the queuing delay.
In particular, if the traffic intensity is close to zero, then packet arrivals are few and far between and it is unlikely that an arriving packet will find another packet in the queue.
Hence, the average queuing delay will be close to zero.
On the other hand, when the traffic intensity is close to 1, there will be intervals of time when the arrival rate exceeds the transmission capacity (due to variations in packet arrival rate), and a queue will form during these periods of time; when the arrival rate is less than the transmission capacity, the length of the queue will shrink.
Nonetheless, as the traffic intensity approaches 1, the average queue length gets larger and larger.

#### Packet Loss

In our discussions above, we have assumed that the queue is capable of holding an infinite number of packets.
In reality a queue preceding a link has finite capacity, although the queuing capacity greatly depends on the router design and cost.
Because the queue capacity is finite, packet delays do not really approach infinity as the traffic intensity approaches 1.
Instead, a packet can arrive to find a full queue.
With no place to store such a packet, a router will **drop** that packet; that is, the packet will be **lost**.

### End-to-End Delay

The delay over a route consisting of $N$ routers is the sum of the delay over every one of the routers.
In addition to processing, transmission, and propagation delays, there can be additional significant delays in the end systems.
For example, an end system wanting to transmit a packet into a shared medium may purposefully delay its transmission as part of its protocol for sharing the medium with other end systems.

## Throughput in Computer Networks

The **throughput** is a measure of the rate (bits/time) at which bits are transferred between a sender and a receiver.
The throughput of a connection will always be limited by the slowest link on the route from the sender to the receiver - this is called the **bottleneck link**.

Generally, the core of the Internet is over-provisioned with high speed links that experience little congestion, so that the rate at which bits can flow from source to destination is constrained by the access network.

## Protocol Layers and Their Service Models

To provide structure to the design of network protocols, network designers organize protocols in **layers**.
A layered architecture allows us to discuss a well-defined, specific part of a large and complex system.
This simplification itself is of considerable value by providing modularity, making it much easier to change the implementation of the service provided by the layer.
As long as the layer provides the same **service** to the layer above it, and uses the same services from the layer below it, the remainder of the system remains unchanged when a layer’s implementation is changed.

One potential drawback of layering is that one layer may duplicate lower-layer functionality.
A second potential drawback is that functionality at one layer may need information that is present only in another layer, which violates the goal of separation of layers.

When taken together, the protocols of the various layers are called the **protocol stack**.
The Internet protocol stack consists of five layers: the physical, link, network, and stack layers.

### Application Layer

The application layer is where network applications and their application-layer protocols reside. 
The Internet’s application layer includes many protocols, such as the HTTP protocol (which provides for Web document request and transfer), SMTP (which provides for the transfer of e-mail messages), FTP (which provides for the transfer of files between two end systems), and DNS (which provides translation from human-friendly names for Internet end systems to 32-bit network addresses).
An application-layer protocol is distributed over multiple end systems, with the application in one end system using the protocol to exchange packets of information with the application in another end system.
We’ll refer to this packet of information at the application layer as a **message**.

### Transport Layer

The Internet’s transport layer transports application-layer messages between application endpoints. In the Internet, there are two transport protocols, TCP and UDP, either of which can transport application-layer messages. 

TCP provides a connection-oriented service to its applications. This service includes guaranteed delivery of application-layer messages to the destination and flow control (that is, sender/receiver speed matching). TCP also breaks long messages into shorter segments and provides a congestion-control mechanism, so that a source throttles its transmission rate when the network is congested. 

The UDP protocol provides a connectionless service to its applications. This is a no-frills service that provides no reliability, no flow control, and no congestion control. 

In this book, we’ll refer to a transport-layer packet as a **segment**.

### Network Layer

The Internet’s network layer is responsible for moving network-layer packets known as **datagrams** from one host to another.
The Internet transport-layer protocol (TCP or UDP) in a source host passes a transport-layer segment and a destination address to the network layer, just as you would give the postal service a letter with a destination address.
The network layer then provides the service of delivering the segment to the transport layer in the destination host.

The Internet’s network layer includes the celebrated IP protocol, which defines the fields in the datagram as well as how the end systems and routers act on these fields.
There is only one IP protocol, and all Internet components that have a network layer must run the IP protocol.
The Internet’s network layer also contains routing protocols that determine the routes that datagrams take between sources and destinations.
The Internet has many routing protocols. The Internet is a network of networks, and within a network, the network administrator can run any routing protocol desired.

### Link Layer

The Internet’s network layer routes a datagram through a series of routers between the source and destination.
To move a packet from one node (host or router) to the next node in the route, the network layer relies on the services of the link layer.
In particular, at each node, the network layer passes the datagram down to the link layer, which delivers the datagram to the next node along the route.
At this next node, the link layer passes the datagram up to the network layer.
Examples of link-layer protocols include Ethernet, WiFi, and the cable access network’s DOCSIS protocol.

### Physical Layer

While the job of the link layer is to move entire frames from one network element to an adjacent network element, the job of the physical layer is to move the individual bits within the frame from one node to the next.
The protocols in this layer are again link dependent and further depend on the actual transmission medium of the link.

## Encapsulation

Similar to end systems, routers and link-layer switches organize their networking hardware and software into layers.
But routers and link-layer switches do not implement all of the layers in the protocol stack; they typically implement only the bottom layers.
Usually, link-layer switches implement layers 1 and 2, while routers implement layers 1 through 3. 
This means, for example, that Internet routers are capable of implementing the IP protocol (a layer 3 protocol), while link-layer switches are not.
This means that while link-layer switches do not recognize IP addresses, they are capable of recognizing layer 2 addresses, such as Ethernet addresses.
Note that hosts implement all five layers; this is consistent with the view that the Internet architecture puts much of its complexity at the edges of the network.

Let's go through the journey of a message from a host to another. 
- At the sending host, an **application-layer message** is passed to the transport layer. 
- In the simplest case, the transport layer takes the message and appends additional information (so-called transport-layer header information) that will be used by the receiver-side transport layer. 
  The application-layer message and the transport-layer header information together constitute the **transport-layer segment**. 
  The transport-layer segment thus encapsulates the application-layer message. 
  The added information might include information allowing the receiver-side transport layer to deliver the message up to the appropriate application, and error-detection bits that allow the receiver to determine whether bits in the message have been changed in route. 
- The transport layer then passes the segment to the network layer, which adds network-layer header information such as source and destination end system addresses, creating a **network-layer datagram**. 
- The datagram is then passed to the link layer, which (of course!) will add its own link-layer header information and create a **link-layer frame**. 

We see that at each layer, a packet has two types of fields: header fields and a **payload field**. 
The payload is typically a packet from the layer above, reflecting the **encapsulation** of the stack protocol.

# Chapter 2: Application Layer

## Principles of Network Applications

At the core of network application development is writing programs that run on different end systems and communicate with each other over the network.
Importantly, to do so, you do not need to write software that runs on network-core devices, such as routers or link-layer switches.
Confining application software to the end systems has facilitated the rapid development and deployment of a vast array of network applications.

### Network Application Architectures

From the application developer’s perspective, the network architecture is fixed and provides a specific set of services to applications. The **application architecture**, on the other hand, is designed by the application developer and dictates how the application is structured over the various end systems.
The two predominant architectural paradigms used in modern network applications are:
- **Client-Server architecture**: there is an always-on host, called the **server**, which services requests from many other hosts, called **clients**.
  Server size needs to scale with size of application. Very big applications require data center(s) to handle the clients' requests.
- **Peer-to-Peer architecture (P2P)**: there is minimal (or no) reliance on dedicated servers. Instead the application exploits direct communication between pairs of intermittently connected hosts, called **peers**.
  One of the most compelling features of P2P architectures is their self-
scalability.

A network application consists of pairs of processes that communicate over a network.
Processes on two different end systems communicate with each other by exchanging **messages** across the computer network.

In the context of a communication session between a pair of processes, the process that initiates the communication is labeled as the **client**, and the process that waits to be contacted is the **server**.

In order for a process running on the client to send packets to a process running on the server, two pieces of information need to be specified: 
- The address of the server host: in the Internet, hosts are identified by **IP addresses**: 32-bit (for IPv4) or 128-bit (for IPv6) values that uniquely identify a host in the Internet.
- An identifier that specifies the receiving process: this is an integer that we give the name **port number**. This is necessary as the server could be running many network applications.

A process sends messages into, and receives messages from, the network through a software interface called a **socket**.
A socket is the interface between the application layer and the transport layer within a host or, in other words, it is the API between the application and the network.
The application developer has control of everything on the application-layer side of the socket but has little control of the transport-layer side of the socket.

The only control that the application developer has on the transport-layer side is (1) the choice of transport protocol and (2) perhaps the ability to fix a few transport-layer parameters such as maximum buffer and maximum segment sizes.
The choice of transport protocol and its parameters may have effects on:
- **data integrity**;
- **throughput**;
- **security of data**;
- **timing**.

There are two main transport layer services that the Internet provides to the application layer.

**TCP**  
The TCP service model includes a connection-oriented service and a reliable data transfer service. When an application invokes TCP as its transport protocol, the application receives both of these services from TCP:
- **Connection-oriented service**. TCP has the client and server exchange transport- layer control information with each other before the application-level mes- sages begin to flow. This so-called **handshaking** procedure alerts the client and server, allowing them to prepare for an onslaught of packets. After the handshaking phase, a **TCP connection** is said to exist between the sockets of the two processes. The connection is a full-duplex connection in that the two processes can send messages to each other over the connection at the same time. When the application finishes sending messages, it must tear down the connection.
- **Reliable data transfer service**. The communicating processes can rely on TCP to deliver all data sent without error and in the proper order. When one side of the application passes a stream of bytes into a socket, it can count on TCP to deliver the same stream of bytes to the receiving socket, with no missing or duplicate bytes.

TCP also includes a congestion-control mechanism, a service for the general welfare of the Internet rather than for the direct benefit of the communicating processes. The TCP congestion-control mechanism throttles a sending process (client or server) when the network is congested between sender and receiver.

**UDP**  
UDP is connectionless, so there is no handshaking before the two processes start to communicate. UDP provides an unreliable data transfer service—that is, when a process sends a message into a UDP socket, UDP provides no guarantee that the message will ever reach the receiving process. Furthermore, messages that do arrive at the receiving process may arrive out of order.
UDP does not include a congestion-control mechanism, so the sending side of UDP can pump data into the layer below (the network layer) at any rate it pleases.

On the application-layer side of the socket, **application-layer protocols** define how an application’s processes, running on different end systems, pass messages to each other. In particular, an application-layer protocol defines:
- The types of messages exchanged, for example, request messages and response messages;
- The syntax of the various message types, such as the fields in the message and how the fields are delineated;
- The semantics of the fields, that is, the meaning of the information in the fields;
- Rules for determining when and how a process sends messages and responds to messages.

Some application-layer protocols, such as HTTP, are specified in RFCs and are therefore in the public domain.

## The Web and HTTP

The **HyperText Transfer Protocol (HTTP)**, the Web’s application-layer protocol, is at the heart of the Web.
HTTP is implemented in two programs: a client program and a server program, executing on different end systems, who talk to each other by exchanging HTTP messages. 
HTTP defines the structure of these messages and how the client and server exchange the messages.

When a user requests a Web page, the browser sends HTTP request messages for the objects in the page to the server.
The server receives the requests and responds with HTTP response messages that contain the objects.

It is important to note that the server sends requested files to clients without storing any state information about the client.
HTTP is thus said to be a **stateless protocol**.

The HTTP protocol uses TCP.

### Persistent and Non-Persistent Connections

In many Internet applications, the client and server communicate for an extended period of time, with the client making a series of requests and the server responding to each of the requests. 
Depending on the application and on how the application is being used, the series of requests may be made back-to-back, periodically at regular intervals, or intermittently.
Consequently, the application developer needs to decide whether to make each request/response pair be sent over a separate TCP connection - **non-persistent connections** (HTTP 1.0) - or if the same TCP connection can be used for all these communications - **persistent connections** (HTTP 1.1).

Persistent connections allow time efficiency in the sending of multiple files sequentially, since they do require much less TCP connections to be established.
For every HTTP request, non-persistent connections need two trips (front and back) to the server for every request (one to establish the TCP connection, and the other for the request/response).
While these can often be done in parallel, persistent connections allow much faster response.
Namely, persistent connections allow for pipelining, where a server will send several pages to the client without waiting for its response.

It must be noted though that for every TCP connection a server has established, it must maintain its state, through TCP buffers and variables.
For a server that is serving many connections, this might be a significant overhead.

### HTTP Message Format

There are two types of HTTP messages: request messages and response messages

#### Request Message

The first line of an HTTP request message is called the **request line**, while the subsequent lines are called the header lines. Depending on the method used in the request message, there might be an **entity body** in the message as well.

![HTTP request message](./figs/HTTP_request_message.png)

The request line has three fields: 
- the method field; 
- the URL field;
- the HTTP version field. 

The method field can take on several different values, including:
- **GET**: used when the browser requests an object (the great majority of HTTP request);
- **HEAD**: similar to the GET method - when a server receives a request with the HEAD method, it responds with an HTTP message but it leaves out the requested object (application developers often use the HEAD method for debugging);
- **POST**: often used when the user fills out a form (for example, when a user provides search words to a search engine). With a POST message, the user is still requesting a Web page from the server, but the contents of it depend on entered data.
- **PUT**: often used in conjunction with Web publishing tools. It allows a user to upload an object to a specific path (directory) on a specific Web server. The PUT method is also used by applications that need to upload objects to Web servers. 
- **DELETE**: allows a user, or an application, to delete an object on a Web server.

### HTTP Response Message

Similarly to a request message, a response message has a **status line**, some **header lines**, and a **entity body** (preceded by a blank line).

![HTTP response message](./figs/HTTP_respnose_message.png)

The header line has three fields:
- the HTTP version field;
- the status code field;
- the phrase field.

This status code and its associated pphrase indicate the result of the request. A few examples are:
- 200 OK: Request succeeded and the information is returned in the response;
- 301 Moved Permanently: Requested object has been permanently moved; 
- 400 Bad Request: This is a generic error code indicating that the request could not be understood by the server;
- 404 Not Found: The requested document does not exist on this server;
- 505 HTTP Version Not Supported: The requested HTTP protocol version is not supported by the server.

## User-Server Interaction: Cookies

**Cookies** allow sites to keep track of users.
Cookie technology has four components: 
- a cookie header line in the HTTP response message;
- a cookie header line in the HTTP request message;
- a cookie file kept on the user’s end system and managed by the user’s browser;
- a back-end database at the Web site.

## Web Caching

A **Web cache**, also called a **proxy server**, is a network entity that satisfies HTTP requests on the behalf of an origin Web server.
Web cache has its own disk storage and keeps copies of recently requested objects in this storage.

When a browser requests an object from a server with an web cache:
1. The browser establishes a TCP connection to the Web cache and sends an HTTP request for the object to the Web cache.
2. The Web cache checks to see if it has a copy of the object stored locally. If it does, the Web cache returns the object within an HTTP response message to the client browser.
3. If the Web cache does not have the object, the Web cache opens a TCP connec- tion to the origin server, that is, to www.someschool.edu. The Web cache then sends an HTTP request for the object into the cache-to-server TCP connec- tion. After receiving this request, the origin server sends the object within an HTTP response to the Web cache.
4. When the Web cache receives the object, it stores a copy in its local storage and sends a copy, within an HTTP response message, to the client browser (over the existing TCP connection between the client browser and the Web cache).

Typically a Web cache is purchased and installed by an ISP.
It has seen deployment in the Internet for two reasons:
- reduce response time;
- reduce traffic

Caching indroduces however a new problem: the copy of an object residing in the cache may have been modified since the copy was cached at the client.
HTTP has a mechanism that allows a cache to verify that its objects are up to date.
This mechanism is called the **conditional GET**.
An HTTP request message is a so-called conditional GET message if it uses the GET method and includes an "If-Modified-Since:" header line.
Upon getting this request, a web cache will request the same page from the original server, which if the page has not been modified since the specified date, will respond with a "304 Not Modified" message (and an empty entity body to save bandwidth), indicating that the web cache may return the object it has stored.

Through the use of **Content Distribution Networks (CDNs)**, Web caches are increasingly playing an important role in the Internet.
A CDN company installs many geographically distributed caches throughout the Internet, thereby localizing much of the traffic.
There are shared CDNs (such as Akamai and Limelight) and dedicated CDNs (such as Google and Netflix).

## HTTP/2

The primary goals for HTTP/2 are:
- to reduce perceived latency by enabling request and response multiplexing over a single TCP connection;
- provide request prioritization and server push;
- provide efficient compression of HTTP header fields.
HTTP/2 does not change HTTP methods, status codes, URLs, or header fields.
Instead, HTTP/2 changes how the data is formatted and transported between the client and server.

!!! TODO !!!
- HOL problem
- HTTP2 solution for HOL

## Eletronic Mail in the Internet

The Internet maiil system has three major components:
- **user agents**;
- **mail servers**;
- **Simple Mail Transfer Protocol (SMTP)**.

When a user A wants to send a message to a user B, A's user agent sends the message to her mail server, where the message is placed in the mail server’s outgoing **message queue**.
When Bob wants to read a message, his user agent retrieves the message from his **mailbox** in his mail server.
How the message goes from A's mail server to B's mail server is defined by SMTP.

SMTP uses TCP to provide reliable transfer of messages.
It is composed of three phases of transfer:
- Handshaking;
- Transfer of messages;
- Closure.

A Mail Message uses the following standard text message format:
- a set of header lines, which may be:
  - "From:" (mandatory)
  - "To:" (mandatory)
  - "Date:"
  - "Subject:"
  - "Received:" (added by receiving SMTP server)
- a blank line;
- the message body (in 7-bit ASCII)

Note that the mailbox of a mail receiver is on a server host, different from the users endpoint.
Therefore, the user needs a protocol to obtain any received mail from the server.
It can't use SMTP, as it is a push protocol.
Some mail access protocols are:
- POP: Post Office Protocol
- IMAP: Internet Mail Access Protocol
- HTTP

## DNS - The Internet's Directory Service

One host is identified by a **hostname**.
Hostnames are mnemonic and are therefore appreciated by humans.
However, hostnames provide little, if any, information about the location within the Internet of the host.
Furthermore, because hostnames can consist of variable-length alphanumeric characters, they would be difficult to process by routers.
For these reasons, hosts are also identified by so-called **IP addresses**.

An IP address consists of four bytes in decimal notation, separated by periods (e.g 121.7.106.83).
It has a rigid hierarchical structure: we scan the address from left to right, and obtain more and more specific information about where the host is located in the Internet.

Because humans prefer hostnames but machines prefer IP addresses, we need a directory service that translates hostnames to IP addresses.
This is the main task of the Internet’s **domain name system (DNS)**.
The DNS is 
- a distributed database implemented in a hierarchy of DNS servers;
- an application-layer protocol that allows hosts to query the distributed database.
The DNS servers are often UNIX machines running the Berkeley Internet Name Domain (BIND) software. 

The DNS protocol runs over UDP and uses port 53.

On top of the standard translation service, DNS is also responsible for:
- **Host aliasing**: A host with a complicated hostname can have one or more alias names. The original hostname is said to be a **canonical hostname**.
- **Mail server aliasing** 
- **Load distribution**: Busy sites are replicated over multiple servers, each server on a different end system with a different IP address. For replicated Web servers, a set of IP addresses is thus associated with one alias hostname. The DNS database contains this set of IP addresses. When clients make a DNS query for a name mapped to a set of addresses, the server responds with the entire set of IP addresses, but rotates the ordering of the addresses within each reply. Because a client typically sends its HTTP request message to the IP address that is listed first in the set, DNS rotation distributes the traffic among the replicated servers.

### Overview of How DNS Works

A simple design for DNS would have one DNS server that contains all the mappings.
This has the following problems:
- Single point of failure;
- Traffic volume;
- Distance centralized database;
- Maintenance issues.

In summary, a centralized database **doesn't scale**.

In order to deal with the issue of scale, the DNS uses a large number of servers, organized in a hierarchical fashion and distributed around the world.
No single DNS server has all of the mappings for all of the hosts in the Internet.
Instead, the mappings are distributed across the DNS servers.
To a first approximation, there are three classes of DNS servers, organized in a hierarchy:
- root DNS servers: there are more than 1000 root servers instances scattered all over the world. These are copies of 13 different root servers.
- top-level domain (TLD) DNS servers: for each of the top-level domains (such as com, org, net, edu, gov, all the country codes, and others) there is a TLD server.
- authoritative DNS servers: every organization with publicly accessible hosts on the Internet must provide publicly accessible DNS records that map the names of those hosts to IP addresses. An organization can choose to implement its own authoritative DNS server to hold these records; alternatively, the organization can pay to have these records stored in an authoritative DNS server of some service provider. Most universities and large companies implement and maintain their own primary and secondary (backup) authoritative DNS server.

There is another important type of DNS server called the local DNS server, also called the **default name server**.
A local DNS server does not strictly belong to the hierarchy of servers but is nevertheless central to the DNS architecture.
Each ISP has a local DNS server, which acts as a proxy for any DNS communication between two hosts. 
When a host connects to an ISP, the ISP provides the host with the IP addresses of one or more of its local DNS servers.

DNS queries can be of two types:
- **Iterative query**: if contacted server doesn't know the mapping for the required hostname, it replies with the name of another server to contact ("I don’t know this name, but ask this server") - burden is always on the client;
- **Recursive query**: if contacted server doesn't know the mapping for the required hostname, it will ask another server for it - burden on the server.

Generally, the query from the requesting host to the local DNS server is recursive, while the remaining queries are iterative.

DNS extensively exploits **DNS caching** in order to improve the delay performance and to reduce the number of DNS messages ricocheting around the Internet.
In a query chain, when a DNS server receives a DNS reply, it can cache the mapping in its local memory.
These cache entries obviously can't be kept indefinitely: they usually disappear after some time (typically 2 days).

### DNS Records

The DNS servers store **resource records (RRs)**, including RRs that provide hostname-to-IP address mappings.
Each DNS reply message carries one or more resource records.

A resource record is a four-tuple that contains the following fields:

(Name, Value, Type, TTL)

TTL is the time to live of the resource record; it determines when a resource should be removed from a cache.

The meaning of Name and Value depend on Type:
- If Type=A, then Name is a hostname and Value is the IP address for the hostname. Thus, a Type A record provides the standard hostname-to-IP address mapping.
- If Type=NS, then Name is a domain and Value is the hostname of an authoritative DNS server that knows how to obtain the IP addresses for hosts in the domain. This record is used to route DNS queries further along in the query chain.
- If Type=CNAME, then Value is a canonical hostname for the alias hostname Name.
- If Type=MX, then Value is the canonical name of a mail server that has an alias hostname Name. Note that by using the MX record, a company can have the same aliased name for its mail server and for one of its other servers (such as its Web server). To obtain the canonical name for the mail server, a DNS client would query for an MX record; to obtain the canonical name for the other server, the DNS client would query for the CNAME record. 

### DNS Messages

There are two kinds of DNS messages: **query** and **reply** messages, and they both have the same format:

- **Header section**: the first 12 bytes of the message.
  The header section has a number of fields.
  The first field is a 16 bit number that identifies the query.
  This identifier is copied from a query to it's reply, allowing the client to match them.
  The second field is the flag field.
  It has, namely, one bit to representer whether the message is a query (0) or a reply (1).
  A 1-bit authoritative flag is set in a reply message when a DNS server is an authoritative server for a queried name.
  A 1-bit recursion-desired flag is set when a client desires that the DNS server perform recursion when it doesn’t have the record.
  1-bit recursion-available field is set in a reply if the DNS server supports recursion.
  In the header, there are also four number-of fields. 
  These fields indicate the number of occurrences of the four types of data sections that follow the header.

- **Question section**:
  Contains information about the query that is being made.
  This section includes (1) a name field that contains the name that is being que- ried, and (2) a type field that indicates the type of question being asked.

- **Answer section**:
  In a reply from a DNS server, the answer section contains the resource records for the name that was originally queried.
  A reply can return multiple RRs in the answer, since a hostname can have multiple IP addresses.

- **Authority section**:
  Contains records of other authoritative servers.

- **Additional section**:
  Other helpful records.

### Inserting Records into the DNS Database

When a new domain name is created, in order for it to be registered in the DNS, a **registrar** needs to verify it's uniqueness and enter it into the DNS database (collecting a fe for its services).
When a domain name is registered, the IP addresses of it's primary and secondary authoritative DNS servers need to be provided.
For each of these two DNS servers, the registrar would then enter into the TLD servers a Type NS and a Type A record.
The creator should then make sure that a Type A resource record for it's Web server and the Type MX resource record for it's mail server are entered into it's authoritative DNS server.

### Dynamic DNS

Dynamic DNS is a method that allows you to notify a Domain Name Server (DNS) to change your active DNS configuration on a device such as a router or computer of its configured hostname and address.
It is most useful when your computer or network obtains a new IP address lease and you would like to dynamically associate a hostname with that address, without having to manually enter the change every time.
Since there are situations where an IP address can change, it helps to have a way of automatically updating hostnames that point to the new address every time.

### DNS Security

Some attacks that have been tried against DNS are:
- DDoS attacks (on root or TLD servers)
- Spoofing attacks

## Peer-to-Peer File Distribution

In this section, we consider a very natural P2P application, namely, distributing a large file from a single server to a large number of hosts (called peers).
In client-server file distribution, the server must send a copy of the file to each of the peers—placing an enormous burden on the server and consuming a large amount of server bandwidth.
In P2P file distribution, each peer can redistribute any portion of the file it has received to any other peers, thereby assisting the server in the distribution process.

Peer-to-Peer file distribution is much more scalable than client-server file distribution.
If we assume:
- a network with abundant bandwith in it's core;
- a server and $N$ clients which are only participating in this transition, and no other network applications, having:
  - $u_s$ upload speed for the server;
  - $u_i$ upload speed and $d_i$ download speed for each of the $N$ clients ($i \in \{1,...,n\}$);
  - a file of size $F$

Then, the **distribution time** for a client-server protocol is

$$
\max \left( \frac{NF}{u_s}, \frac{F}{d_{min}} \right)
$$

where $d_{min} = \min (d_1, ..., d_n)$ and, for the P2P protocol it is

$$
\max \left( \frac{F}{u_s}, \frac{F}{d_{min}}, \frac{NF}{u_s + \sum_{i=1}^N u_i} \right)
$$

# Chapter 3: Transport Layer

A transport-layer protocol provides for **logical communication** between application processes running on different hosts - that is, from an application’s perspective, it is as if the hosts running the processes were directly connected.
The transport-layer is then responsible for converting application-layer messages into transport-layer **segments**.

The transport-layer's services are conditioned by the network-layer.
The Internet’s network-layer protocol has a name - IP, for Internet Protocol. 
IP provides logical communication between hosts.
The IP service model is a **best-effort delivery service**. 
This means that IP makes its “best effort” to deliver segments between communicating hosts, but it makes no guarantees.
In particular, it does not guarantee:
- segment delivery;
- orderly delivery of segments;
- integrity of the data in the segments.

For these reasons, IP is said to be an unreliable service.

The most fundamental responsibility of UDP and TCP is to extend IP’s delivery service between two end systems to a delivery service between two processes running on the end systems.
Extending host-to-host delivery to process-to-process delivery is called transport-layer **multiplexing** and **demultiplexing**.
UDP and TCP also provide integrity checking by including error-detection fields in their segments’ headers.

These two minimal transport-layer services are the only two services that UDP provides.
TCP, on the other hand, converts IP’s unreliable service between end systems into a reliable data transport service between processes.
TCP also provides **congestion control**.

## Multiplexing and Demultiplexing

First, we recall that a process can have one or more **sockets**, through which the communication between a process and the network is implemented.
Thus, the transport layer must actually multiplex and demultiplex between sockets, and not processes.
These sockets have a unique identifier, which corresponds to the **port number**.

UDP multiplexing and demultiplexing is very simple.
When it has to deliver an application-layer message, UDP places in the corresponding segment's header a source port number and a destination port number.
It then passes the segment on to the network-layer, which will find the destination's IP address, place it somewhere in it's datagram's header, and forward such datagram to such IP address.
Note that any socket is uniquely identified by it's IP address and it's port number.
On the receiving end, the destination host receives a segment from the network-layer and finds in it's header the socket it needs to forward the application-layer message to.

Note that, unlike an UDP socket, a TCP socket is identified by four values: the destination's IP address and port number and the source's IP address and port number.
In particular, and in contrast with UDP, two arriving TCP segments with different source IP addresses or source port numbers will be directed to two different sockets.
After a connection is established between a server and a client, the socket corresponding to that connection will be identified by those four values, and any segment with them will be matched to it.

## Connectionless Transport: UDP

UDP is a simple "bare bones" Internet transport protocol that does few more than pass application-layer messages to the network layers.
As we've seen, such a protocol must at least provide a multiplexing and demultiplexing service, and that, on top of that, UDP also provides a very simple error-checking server.
Nevertheless, UDP is an unreliable service.

It has the following advantages:

- Finer application-level **control over what data is sent**, and when;
- **No connection establishment** implies no delay on message sending;
- **No connection state** allows a server to support more active clients;
- **Small packet header overhead**.

Common applications that run over UDP are **DNS**, **SNMP**, **HTTP/3** and multimedia applications such as Internet phone, real-time video conferencing and streaming of stored audio and video.
Often, these applications might implement reliability themselves, enjoying UDP's advantages while having more guarantees.

An UDP segment is composed of the following fields:

- an header with four fields:
  - **source port** number
  - **destination port** number
  - **length** of the data field
  - **checksum**, used for error-checking
- the **data field**, with the application message

The checksum field is obtained by splitting the segment in a sequence of 16-bit values and adding them as 16-bit integers (considering overflow).
The receiver needs to compute the checksum of the data field similarly. 
If these values differ, then there was an error.
Note that UDP does not have error correction, only error detection.

## Principles of Reliable Data Transfer

It is the responsibility of a reliable data transfer protocol to implement this service abstraction.
This task is made difficult by the fact that the layer below the reliable data transfer protocol may be unreliable.

We'll step through a series of protocols, each one becoming more complex, arriving at a flawless, reliable data transfer protocol.

### Building a Reliable Data Transfer Protocol

#### Reliable Data Transfer over a Perfectly Reliable Channel: rdt1.0

We first consider the simplest case, in which the underlying channel is completely reliable.
The protocol in this case is trivial.
The **finite-state machine (FSM)** definitions for the rdt1.0 sender and receiver are shown below.

![rdt1.0: sending side](./figs/rtp1.0_sender_fsm.png)
![rdt1.0: receiving side](./figs/rtp1.0_receiver_fsm.png)

#### Reliable Data Transfer over a Channel with Bit Errors: rdt2.0

Now we'll consider the case where bit errors might occur in an unreliable lower level communication channel.
However, we'll continue to assume that all transmitted packets are received in the order in which they were sent.

The keys for this protocol are:
- receiver has a method of **error detection**;
- receiver is able to send positive (**ACK**) or negative (**NAK**) **feedback** to sender;
- sender is able to **retransmit** a packet.

![rdt2.0: sending side](./figs/rtp2.0_sender_fsm.png)
![rdt2.0: receiving side](./figs/rtp2.0_receiver_fsm.png)

Note that we need to account for the possibility of corruption on the receiver feedback.
We might handle this in the following ways:
- Ask for the receiver to repeat the feedback. 
  This message might however be corrupted too, and thus we'd need another message recursively;
- Add enough checksum bits to allow the sender not only to detect, but also to recover from, bit errors.
- Simply resend the current data packet when the sender receives a garbled feedback packet.
  This approach, however, introduces duplicate packets into the sender-to-receiver channel. 
  The fundamental difficulty with duplicate packets is that the receiver doesn't know whether it's feedback was received correctly at the sender. 
  Thus, it cannot know whether an arriving packet contains new data or is a retransmission.
  This can be solved by asking the sender to add a **sequence number** field.
  For this simple case of a stop-and-wait protocol, a 1-bit sequence number will suffice.
  Since we are currently assuming a channel that does not lose packets, the feedback does not need to indicate the sequence number of the packet it corresponds to.

![rdt2.1: sending side](./figs/rtp2.1_sender_fsm.png)
![rdt2.1: receiving side](./figs/rtp2.1_receiver_fsm.png)

We can achieve the same functionality without using NAK.
If the receiver sends always an ACK for the last well received packet, the sender can infer if the last packet was well received.
Of course, now, the receiver must include the sequence number in the feedback message.

![rdt2.2: sending side](./figs/rtp2.2_sender_fsm.png)
![rdt2.2: receiving side](./figs/rtp2.2_receiver_fsm.png)

#### Reliable Data Transfer over a Lossy Channel with Bit Errors: rdt3.0

Suppose now that in addition to corrupting bits, the underlying channel can lose
packets as well.

One possible approach would be the sender wait until it is sure that a packet must've been lost (either the one it sent, or the response).
The problems it this approach is that it is hard to estimate a worst-case response time, much less know for sure.
Moreover, the protocol should ideally recover from packet loss as soon as possible.

The approach thus adopted in practice is for the sender to judiciously choose a time value such that packet loss is likely, although not guaranteed, to have happened.
If an ACK is not received within this time, the packet is retransmitted.
This introduces the possibility of **duplicate data packets** in the sender-to-receiver channel, which can already be dealt with the functionality introduced in rdt2.2.

Implementing a time-based retransmission mechanism requires a countdown timer that can
interrupt the sender after a given amount of time has expired.

![rdt3.0: sending side](./figs/rtp3.0_sender_fsm.png)

### Pipelined Reliable Data Transfer Protocols

The protocols seen above display very poor performance.
In order to send a message of $L$ bits at a rate of $R$ bits/sec, the sender will only be using the sending channel $\frac{L/R}{RTT + L/R}$ of the time.
For long distances between hosts, this can be an extremely low fraction.

To improve performance, RDT protocols use **pipelining**.
Pipelining requires increasing the range of sequence numbers and buffering packets both at the sender and at the receiver.
The requirements in both these aspects depend on how the protocol responds to lost, corrupted, and overly delayed packets.

Two basic approaches toward pipelined error recovery can be identified: **Go-Back-N** and **selective repeat**.
These are both called **sliding window protocols** as they allow the sender to transmit up to $N$ packets without waiting for an acknowledgement.
The value $N$ is called the **window size**.

#### Go-Back-N (GBN)

[TODO]

![gbn: sending side](./figs/gbn_sender_fsm.png)
![gbn: receiving side](./figs/gbn_receiver_fsm.png)

#### Selective Repeat

[TODO]

## Connection Oriented Transport: TCP

## Principles of Congestion Control

## TCP Congestion Control

# Chapter 4: The Network Layer

The **Network Layer** is responsible for transporting segments from sending to receiving host.
The sending side encapsulates transport layer segments into **datagrams**, and the receiving side extracts such segments and delivers it to the transport layer.
Network layer protocols are implemented in *every host* and router.

The Network Layer can be split into two interacting parts:
- the **data plane** determines the *per-router* functions in the network layer that determine how a datagram moves from a router's **input link** to it's **output link**. This is called **forwarding**.
- the **control plane** determines the *network-wide* logic that controls how a datagram is routed among routers along an end-to-end path from the source host to the destination host. This is called **routing**.

A key element in every network router is its **forwarding table**.
A router forwards a packet by examining the value of one or more fields in the arriving packet’s header, and then using these header values to index into its forwarding table.
The value stored in the forwarding table entry for those values indicates the outgoing link interface at that router to which that packet is to be forwarded.

The content of a forwarding table is determined by the routing algorithm.
Traditionally, a routing algorithm would run on every single router and it would communicate with other router's algorithm.
Alternitavely, **Software-Defined Networking (SDN)** is often used, where the routing a **remote controller** determines a routing algorithm, and communicates it to the routers, distributing forwarding tables.
The remote controller might be implemented in a remote data center with high reliability and redundancy, and might be managed by the ISP or some third party.

## The Internet Protocol (IP)

### IPv4 Datagram

The key fields in the IPv4 datagram are the following:
- **Version number**: specify the IP protocol in use, allowing the router to determine how to interpret the remainder of the IP datagram.
- **Header length**: because an IPv4 datagram can contain a variable number of options, 4 bits are needed to determine where the payload actually begins.
- **Type of service**: allow different types of IP datagrams to be distinguished from each other (for example, real-time datagrams from non-real-time traffic).
- **Datagram length**: total length of the IP datagram (header plus data), measured in bytes. Since this field is 16 bits long, the theoretical maximum size of the IP datagram is 65,535 bytes. However, datagrams are rarely larger than 1500 bytes.
- **Identifier, flags, fragmentation offset**: these three fields have to do with so-called IP fragmentation, when a large IP datagram is broken into several smaller IP datagrams which are then forwarded independently to the destination, where they are reassembled
- **Time-to-live**: ensure that datagrams do not circulate forever in the network. This field is decremented by one each time the datagram is processed by a router, being dropped if it reaches 0.
- **Protocol**: indicates the specific transport-layer protocol to which the data portion of this IP datagram should be passed.
- **Header checksum**: aids a router in detecting bit errors in a received IP datagram.
- **Source and destination IP addresses**.
- **Options**: allow an IP header to be extended. Header options were meant to be used rarely—hence the decision to save overhead by not including the information in options fields in every datagram header. However, the mere existence of options does complicate matters—since datagram headers can be of variable length, one cannot determine a priori where the data field will start. Also, since some datagrams may require options processing and others may not, the amount of time needed to process an IP datagram at a router can vary greatly. These considerations become particularly important for IP processing in high- performance routers and hosts.
- **Data (payload)**.

![IPv4 datagram format](./figs/ipv4_datagram.png)

#### Fragmentation

// TODO

### IPv4 Addressing

Each IP address is 32 bits (4 bytes) long, meaning that there are $2^{32}$ possible IP addresses.
These addresses are typically written in so-called dotted-decimal notation (for example 192.168.80.30).

Every **interface** (connection between host/router and physical link) on every host and router in the global Internet must have an IP address that is globally unique.
That means, for example, that a router has several IP addresses associated with it.
This makes sense as the router's function is to allow hosts on different subnets (also called an IP network or simply network) to communicate.
A **subnet** is a set of device interfaces that can physically reach each other without passing through a router.
These are assigned an address, sometimes known as a **subnet mask**, of the form 223.1.1.0/24 where the /24 indicates that the leftmost 24 bits of the IP address shall be the same for every host on that subnet.

The Internet’s address assignment strategy is known as **Classless Interdomain Routing (CIDR)**, which generalizes the notion of subnet addressing.
As with subnet addressing, the 32-bit IP address is divided into two parts and again has the dotted-decimal form a.b.c.d/x, where x indicates the number of bits in the first part of the address.
The x most significant bits of an address of the form a.b.c.d/x constitute the network portion of the IP address, and are often referred to as the **prefix** or **network prefix** of the address.
IP addresses of devices within the organization will share the common prefix.  
The remaining 32-x bits of an address can be thought of as distinguishing among the devices within the organization, all of which have the same network prefix. 
These are the bits that will be considered when forwarding packets at routers within the organization.

A router outside the organization's ISP need not know that a message is destined to such organization.
Therefore, it can use only the prefix to redirect the message to the ISP's network.
This ability to use a single prefix to advertise multiple networks is often referred to as **address aggregation** (also **route aggregation** or **route summarization**).

Note that getting an IP address from an ISP means that, if an organization wants to change ISP, it needs to change IP.
Actually, this problem is circumvented by informing the organization's new ISP to advertise the organization's subnet (on top of it's own IP).
For this solution to work, every router must always opt for the most specific subnet on it's forwarding table.

Before CIDR was adopted, the network portions of an IP address were constrained
to be 8, 16, or 24 bits in length, an addressing scheme known as **classful addressing**.

An organization can obtain a block of IP addresses for use within an organization’s subnet by contacting it's ISP, which would provide addresses from a larger block of addresses that had already been allocated to the ISP.
The ISPs themselves obtain their address blocks from the **Internet Corporation for Assigned Names and Numbers (ICANN)**.
The role of the ICANN is to:
- allocate IP addresses;
- manage DNS root servers;
- assigning domain names and resolving domain name disputes.

### DHCP: Dynamic Host Configuration Protocol

Once an organization has obtained a block of addresses, it can assign individual IP addresses to the host and router interfaces in its organization.
A system administrator will typically manually configure the IP addresses into the router.
Host addresses can also be configured manually, but typically this is done using the **Dynamic Host Configuration Protocol (DHCP)**.

DHCP allows a host to obtain (be allocated) an IP address automatically.
A network administrator can configure DHCP so that a given host receives the same IP address each time it connects to the network, or a host may be assigned a temporary IP address that will be different each time the host connects to the network.

Because of DHCP’s ability to automate the network-related aspects of connecting a host into a network, it is often referred to as a **plug-and-play** or **zeroconf** (zero-configuration) protocol. 
This capability makes it very attractive to the network administrator who would otherwise have to perform these tasks manually!
DHCP is also enjoying widespread use in networks where hosts join and leave the network frequently.

DHCP is a client-server protocol.
A client is typically a newly arriving host wanting to obtain network configuration information, including an IP address for itself.
In the simplest case, each subnet will have a DHCP server.
If no server is present on the subnet, a DHCP relay agent (typically a router) that knows the address of a DHCP server for that network is needed.

Obtaining an IP address through DHCP is a 4-step process:
- Host broadcasts **DHCP discover** message, to find a DHCP server;
- DHCP server responds with **DHCP offer** message, where it provides the host with an IP address that it can use;
- Host requests such IP address through a **DHCP request** message;
- DHCP server confirms that the host can start using such IP address through a **DHCP ACK** message.

On the DHCP offer message, the DHCP server includes a **lease time** - the amount of time that the host is allowed to use that IP address.
If, after some time, the host wants to keep using the IP address, it can renew it.
For this, the host only needs to send the DHCP request message, to which the server will reply with DHCP ACK, informing the client that it's lease has been extended.
The client should try and renew it's lease after 50% of the lease time has passed (T1 time). 
If this first time, it should try again after 85% of the lease time has passed (T2 time).
When the lease time expires, the client should stop using the leased address.

It is important to note that DHCP is an **application layer protocol**.

### ICMP: The Internet Control Message Protocol

The Internet Control Message Protocol (ICMP) is used by hosts and routers to communicate network-layer information to each other.
The most typical use of ICMP is for error reporting.
ICMP is often considered part of IP, but architecturally it lies just above IP, as ICMP messages are carried inside IP datagrams.
ICMP messages have a type and a code field, and contain the header and the first 8 bytes of the IP datagram that caused the ICMP message to be generated.

### Network Address Translation (NAT)

With the proliferation of small office and home office subnets, it would seem that whenever one of these wants to install a LAN to connect multiple machines, a range of addresses would need to be allocated by the ISP to cover all IP devices.
If the subnet grew bigger, a larger block of addresses would have to be allocated.
**Network Address Translation (NAT)**, however, provides a simple solution to assign IP addresses inside a private subnet.

NAT works by assigning to all interfaces within a private network an address with the subnet mask 10.0.0.0/24. 
The address space 10.0.0.0/8 is reserved for **private networks**, and thus, every IP address with this mask will only make sense within a host's subnet.

The NAT-enabled router does not look like a router to the outside world.
Instead the NAT router behaves to the outside world as a single device with a single IP address.
Whenever a host with a private address wants to send a message to outside it's subnet, it sends such message to the router, that masks the message behind it's IP address.
The router can also forward packets arriving to the correct hosts by using a **NAT translation table** and including port numbers and IP addresses in the table entries.

NAT is controversial because it:
- Is a network layer protocol and changes information on the transport layer, such as port numbers.
- Violates end-to-end principle, as an application designer might need to take NAT into account when designing it's application. For example, server processes wait for incoming requests at well-known port numbers and peers in a P2P protocol need to accept incoming connections when acting as servers. Technical solutions to these problems include **NAT traversal** tools.

### IPv6

In the early 1990s, the Internet Engineering Task Force began an effort to develop a successor to the IPv4 protocol.
A prime motivation for this effort was the realization that the 32-bit IPv4 address space was beginning to be used up, with new subnets and IP nodes being attached to the Internet (and being allocated unique IP addresses) at a breathtaking rate.
To respond to this need for a large IP address space, a new IP protocol, IPv6, was developed.
The designers of IPv6 also took this opportunity to tweak and augment other aspects of IPv4, based on the accumulated operational experience with IPv4.

The most important changes introduced in IPv6 are:
- **Expanded addressing capabilities**: IP address size increases from 32 to 128 bits.
- **A streamlined 40-byte header**: a number of IPv4 fields have been dropped or made optional. The resulting 40-byte fixed-length header allows for faster processing of the IP datagram by a router.
- **Flow labeling**: “labeling of packets belonging to particular flows for which the sender requests special handling, such as a non-default quality of service or real-time service.”

The IPv6 datagram contains the following fields:
- **Version**: 4-bit field identifies the IP version number.
- **Traffic class**: 8-bit traffic class field, like the TOS field in IPv4, can be used to give priority to certain datagrams.
- **Next header**: identifies the protocol to which the contents of this datagram will be delivered (for example, to TCP or UDP).
- **Hop limit**: like TTL, the contents of this field are decremented by one by each router that forwards the datagram. If the hop limit count reaches zero, a router must discard that datagram.
- **Source and destination addresses**.
- **Data**.

![IPv6 datagram format](./figs/ipv6_datagram.png)

We highlight that the following fields disappeared from IPv4 to IPv6:
- **Fragmentation/reassembly**: IPv6 does not allow for fragmentation and reassembly at intermediate routers; these operations can be performed only by the source and destination. If an IPv6 datagram received by a router is too large to be for- warded over the outgoing link, the router simply drops the datagram and sends a “Packet Too Big” ICMP error message (see Section 5.6) back to the sender. The sender can then resend the data, using a smaller IP datagram size. Fragmentation and reassembly is a time-consuming operation; removing this functionality from the routers and placing it squarely in the end systems considerably speeds up IP forwarding within the network.
- **Header checksum**. Because the transport-layer (for example, TCP and UDP) and link-layer (for example, Ethernet) protocols in the Internet layers perform check- summing, the designers of IP probably felt that this functionality was sufficiently redundant in the network layer that it could be removed. Once again, fast processing of IP packets was a central concern.
- **Options**. An options field is no longer a part of the standard IP header. However, it has not gone away. Instead, the options field is one of the possible next headers pointed to from within the IPv6 header. That is, just as TCP or UDP protocol headers can be the next header within an IP packet, so too can an options field. The removal of the options field results in a fixed-length, 40-byte IP header.

// TODO: casting cenas

#### Transitioning from IPv4 to IPv6

How can the public Internet, which is based on IPv4, be transitioned to IPv6?
The problem is that while new IPv6-capable systems can be made backward-compatible, that is, can send, route, and receive IPv4 datagrams, already deployed IPv4-capable systems are not capable of handling IPv6 datagrams.  
One option would be to declare a flag day—a given time and date when all Internet machines would be turned off and upgraded from IPv4 to IPv6.
This is impossible on an Internet with billions of connected devices.
Another solution would be to translate IPv6 headers to IPv4 headers, but this would imply some loss of information.

The approach to IPv4-to-IPv6 transition that has been most widely adopted in practice involves **tunneling**.
Assume that we want to send an IPv6 datagram between to IPv6 supporting nodes, through a set of IPv4 routers, which we refer to as the **tunnel**.
A solution is to just take the IPv6 datagram, encapsulate it with a IPv4 header, and send it through the tunnel.

## Routing Algorithms

A routing algorithm is often looking for the **least-cost path** from a host to another on the network graph.
This graph has the network's routers as vertices and the physical links between routers as edges.
Of course the cost of an edge depends on the task that we want to perform.
It might for example, depend bandwidth, delay time, monetary cost, etc.

A routing algorithm might be:
- **centralized** or **global**: the algorithm takes the connectivity between all nodes and all link costs as inputs. The calculation can be run at one site or replicated in every router.
- **decentralized**: the calculation of the least-cost path is carried out in an iterative, distributed manner by the routers. No node has complete information about the costs of all network links. Instead, each node begins with only the knowledge of the costs of its own directly attached links. Then, through an iterative process of calculation and exchange of information with its neighboring nodes, a node gradually calculates the least-cost path to a destination or set of destinations.

A routing algorithm can also be classified as:
- **static**: routes change very slowly over time, often as a result of human intervention.
 - **dynamic**: the routing paths change as the network traffic loads or topology change. While dynamic algorithms are more responsive to network changes, they are also more susceptible to problems such as routing loops and route oscillation.

 Finally, we also differentiate between algorithms that are:
 - **load-sensitive**: link costs vary dynamically to reflect the current level of congestion in the underlying link.
 - **load-insensitive**: a link’s cost does not explicitly reflect its current (or recent past) level of congestion.

### Link State (LS) Routing Algorithm

The **Link State (LS)** routing algorithm is a centralized algorithm, where every node obtains information about the network's topology by having each node broadcast link-state packets (LSP) to it.
This algorithm then uses Dijkstra's algorithm to compute the least-cost path from the source node to every other node.

### Distance Vector (DV) Routing Algorithm

The **Distance Vector (DV)** routing algorithm is a decentralized algorithm. It is:
- **distributed**: each node receives some information from one or more of its directly attached neighbors, performs a calculation, and then distributes the results of its calculation back to its neighbors.
- **iterative**: the algorithm goes on until no more information is exchanged between neighbors.
- **asynchronous**: it does not require all of the nodes to operate in lockstep with each other.

It consists on an application of the Bellman-Ford algorithm to the network graph.

// TODO: understand count to infinity problem and poisoned reverse solution

### Comparison of LS and DV

We observe the following differences:
- Message complexity: the LS algorithm requires $O(NE)$ messages to be sent (every node must broadcast it's forwarding table), while the DV algorithm only requires exchanges between neighbours.
- Speed of Convergence: the LS algorithm converges in $O(N^2)$ while the DV algorithm's convergence time varies (may temporarily have routing loops and suffers from the count to infinity problem).
- Robustness: the LS algorithm is more robust, as each node only calculates the cost of a link, making failures more isolated. The DV algorithm, however, computes path's costs, meaning that errors can propagate through the network.

## Routing in the Internet

### Hierarchical Routing

The above algorithms viewed the network was a collection of connected indistinguishable routers.
However, this model is impractical for two important reasons: 
- **Scale**: with hundreds of millions of routers in the internet, the above algorithms would require enormous amounts of time and memory to work;
- **Administrative autonomy**: each ISP generally wants to operate its network as it pleases, or to hide aspects of its network's internal organization from the outside.

Both of these problems can be solved by organizing routers into **autonomous systems (ASs)**, with each AS consisting of a group of routers that are under the same administrative control.
Often the routers in an ISP, and the links that interconnect them, constitute a single AS but some ISPs partition their network into multiple ASs.
Every router in the same AS runs the same **intra-autonomous system routing protocol**.

Hierarchical routing thus works as follows:
When a host wants to send a message to another host, it sends the message to the AS, who then forwards it to the destination network, who can finally reach the destination host.

// TODO

### Intra-AS Routing

Intra-AS routing protocols are also known as **Interior Gateway Protocols (IGP)**. 
The most common ones are:
- **RIP**: Routing Information Protocol;
- **OSPF**: Open Shortest Path First;
- **IGRP**: Interior Gateway Routing Protocol (Cisco proprietary).

#### Routing Information Protocol (RIP)

The RIP is a DV algorithm that uses the number of hops (routers along the way) as the distance metric.
It sets a maximum distance of 15 hops for any message.
The routers exchange distance vectors every 30 seconds, via response messages, also called **advertisement**.
Each advertisement lists up to 25 destination subnets within the AS.
If no advertisement is heard from a router after 180 seconds, it's declared dead and any route via such router is invalidated.
The remaining nodes (starting by the dead node's neighbours) start advertising the event, and eventually the link failure propagates to the entire network.

#### Open Shortest Path First (OSPF)

OSPF is a link-state protocol that uses flooding of link-state information and a Dijkstra’s least-cost path algorithm.
With OSPF, each router constructs a complete topological map (that is, a graph) of the entire autonomous system.
Each router then locally runs Dijkstra’s shortest-path algorithm to determine a shortest-path tree to all subnets, with itself as the root node.

With OSPF, a router broadcasts routing information to all other routers in the autonomous system, not just to its neighboring routers.
A router broadcasts link-state information whenever there is a change in a link’s state or periodically, even if the link’s state has not changed.  
OSPF advertisements are contained in OSPF messages that are carried directly by IP.
Thus, the OSPF protocol must itself implement functionality such as reliable message transfer and link-state broadcast.

OSPF offers the following features:
- **Security**: all OSPF messages are authenticated, preventing malicious intrusion.
- **Multiple same-cost paths**: OSPF allows multiple same-cost paths to be chosen.
- **Integrated support for unicast and multicast routing**: Multicast OSPF (MOSPF) provides simple extensions to OSPF to provide for multicast routing. MOSPF uses the existing OSPF link database and adds a new type of link-state advertisement to the existing OSPF link-state broadcast mechanism.
- **Support for hierarchy within a single AS**: An OSPF autonomous system can be configured hierarchically into areas. Each area runs its own OSPF link-state routing algorithm, with each router in an area broadcasting its link state to all other routers in that area. Within each area, one or more area border routers are responsible for routing packets outside the area. Lastly, exactly one OSPF area in the AS is configured to be the backbone area. The primary role of the backbone area is to route traffic between the other areas in the AS. The backbone always contains all area border routers in the AS and may contain non-border routers as well. Inter-area routing within the AS requires that the packet be first routed to an area border router (intra-area routing), then routed through the backbone to the area border router that is in the destination area, and then routed to the final destination.

### Inter-AS Routing

In order for devices on multiple AS to communicate, the entire Internet must use the same **inter-autonomous system routing protocol**.
In the current Internet, the protocol used is known as the **Border Gateway Protocol (BGP)**.

### Border Gateway Protocol (BGP)

As an inter-AS routing protocol, BGP provides each router a means to:
- Obtain prefix reachability information from neighboring ASs.
- Determine the "best" routes to the prefixes.

For each AS, each router is either a gateway router or an internal router.
A gateway router is a router on the edge of an AS that directly connects to one or more routers in other ASs.
An internal router connects only to hosts and routers within its own AS.

In BGP, pairs of routers exchange routing information over semi-permanent TCP connections.
Each such TCP connection, along with all the **BGP messages** sent over the connection, is called a **BGP connection**.
Furthermore, a BGP connection that spans two ASs is called an **external BGP (eBGP)** connection, and a BGP session between routers in the same AS is called an **internal BGP (iBGP)** connection.
There is typically one eBGP connection for each link that directly connects gateway routers in different ASs.  
Note that iBGP connections do not always correspond to physical links.

BGP messages can be of the following types:
- **OPEN**: opens TCP connection to remote BGP peer and authenticates sending BGP peer;
- **UPDATE**: advertises new path (or withdraws old);
- **KEEPALIVE**: keeps connection alive in absence of UPDATES. Also ACKs OPEN request;
- **NOTIFICATION**: reports errors in previous messages or closes connection.

When a router advertises a prefix across a BGP connection, it includes with the prefix several **BGP attributes**.
In BGP jargon, a prefix along with its attributes is called a **route**.
Two of the more important attributes are:
- **AS-PATH**: contains the list of ASs through which the advertisement has passed. To generate the AS-PATH value, when a prefix is passed to an AS, the AS adds its ASN to the existing list in the AS-PATH. BGP routers also use the AS-PATH attribute to detect and prevent looping advertisements.
- **NEXT-HOP**: the IP address of the router interface that begins the AS-PATH.

#### Hot Potato Routing

In hot potato routing, the route chosen is that route with the least cost to the NEXT-HOP router beginning that route.
Therefore, the steps for adding an outside-AS prefix in a router’s forwarding table are the following:
- Learn from inter-AS protocol that subnet x is reachable via multiple gateways.
- Use routing info from intra-AS protocol to determine costs of least-cost paths to each of the gateways.
- Hot potato routing: Choose the gateway that has the smallest least cost.
- Determine from forwarding table the interface I that leads to least-cost gateway. Enter (x,I) in forwarding table.

#### Route-Selection Algorithm

In practice, BGP uses an algorithm that is more complicated than hot potato routing, but nevertheless incorporates hot potato routing.
For any given destination prefix, the input into BGP’s route-selection algorithm is the set of all routes to that prefix that have been learned and accepted by the router.
If there are two or more routes to the same prefix, then BGP sequentially invokes the following elimination rules until one route remains:
1. A route is assigned a local preference value as one of its attributes. The value of the local preference attribute is a policy decision that is left entirely up to the AS’s network administrator. The routes with the highest local preference values remain.
2. The routes with the shortest AS-PATH are selected. If this were the only rule for selection, then BGP would be using a DV algorithm where the distance metric uses the number of AS hops.
3. Hot potato routing is used, that is, the routes with the closest NEXT-HOP router are selected.
4. If more than one route still remains, the router uses BGP identifiers to select the route.

Note that an ISP might not be incentivized to advertise certain routes, as other ISPs could use that information to route their traffic through the competition, saving bandwidth.
This is why company policy is the first criteria for route selection.
Typically, any traffic flowing across an ISP’s backbone network must have either a source or a destination (or both) in a network that is a customer of that ISP.

### IP-Anycast

In many applications, we are interested in 
- replicating the same content on different servers in many different dispersed geographical locations; 
- having each user access the content from the server that is closest.

BGP’s route-selection algorithm provides an easy and natural mechanism for doing so.
During the IP-anycast configuration stage, an entity with multiple servers can assign the same IP address to each of its servers, and uses standard BGP to advertise this IP address from each of the servers. 
When a BGP router receives multiple route advertisements for this IP address, it treats these advertisements as providing different paths to the same physical location (when, in fact, the advertisements are for different paths to different physical locations).
When configuring its routing table, each router will locally use the BGP route-selection algorithm to pick the “best” route to that IP address.

CDNs generally choose not to use IP-anycast because BGP routing changes can result in different packets of the same TCP connection arriving at different instances of the Web server.
However, it is extensively used to direct DNS queries to the closest root DNS server.

// TODO: broadcasting, multicasting, spanning trees

# The Link Layer and LANs

In this chapter we'll refer to any device that runs a link-layer protocol as a **node**.
Nodes include hosts, routers, switches, and WiFi access points.
We will also refer to the communication channels that connect adjacent nodes along the communication path as links.
Any link-layer protocol provides the basic service of transporting a datagram from a node to another.
However, different protocols may or may not offer the following services:
- **Framing**: Almost all link-layer protocols encapsulate each network-layer datagram within a **link-layer frame** before transmission over the link.
- **Link Access**: A medium access control (MAC) protocol specifies the rules by which a frame is transmitted onto the link. For point-to-point links that have a single sender at one end of the link and a single receiver at the other end of the link, the MAC protocol is simple. The more interesting case is when multiple nodes share a single broadcast link—the so-called multiple access problem.
- **Reliable Delivery**: When a link-layer protocol provides reliable delivery service, it guarantees to move each network-layer datagram across the link without error. A link-layer reliable delivery service is often used for links that are prone to high error rates, such as a wireless link, with the goal of correcting an error locally, rather than forcing an end-to-end retransmission of the data by a transport- or application-layer protocol. However, link-layer reliable delivery can be considered an unnecessary overhead for low bit-error links, including fiber, coax, and many twisted-pair copper links.
- **Error Detection and Correction**: Error detection in the link layer is usually more sophisticated and is implemented in hardware.
- **Flow Control**: To adjust pace between adjacent sending and receiving nodes;
- **Half-Duplex and Full-Duplex Links**: With half duplex, nodes at both ends of link can transmit, but not at the same time.

The Ethernet capabilities of a host are either integrated into the motherboard chipset or implemented via a low-cost dedicated Ethernet chip.
For the most part, the link layer is implemented on a chip called the **network adapter**, also sometimes known as a **network interface controller (NIC)**.
The network adapter implements many link layer services including framing, link access, error detection, and so on. Thus, much of a link-layer controller’s functionality is implemented in hardware.

On the sending side, the controller takes a datagram that has been created and stored in host memory by the higher layers of the protocol stack, encapsulates the datagram in a link-layer frame (filling in the frame’s various fields), and then transmits the frame into the communication link, following the link-access protocol.  
On the receiving side, a controller receives the entire frame, and extracts the network-layer datagram. If the link layer performs error detection, then it is the sending controller that sets the error-detection bits in the frame header and it is the receiving controller that performs error detection.

## Link-Layer Addressing and ARP

Every node with a network interface has a link layer address.
A host or router with multiple network interfaces will thus have multiple link-layer addresses associated with it, just as it would also have multiple IP addresses associated with it.
A link-layer address is variously called a **LAN address**, a **physical address**, or a **MAC address**.
For most LANs, the MAC address is 6 bytes long, giving 248 possible MAC addresses.
These 6-byte addresses are typically expressed in hexadecimal notation, with each byte of the address expressed as a pair of hexadecimal numbers.  
No two adapters have the same address.
The MAC address space is managed by the IEEE, who guarantees that no two companies are manufacturing adapters with equivalent addresses.
The IEEE does this by selling batches of $2^{24}$ addresses for a nominal fee: it fixes the first 24 bits of a MAC address and lets a company create unique combinations of the last 24 bits for each adapter.  
An adapter’s MAC address has a flat structure (as opposed to a hierarchical structure) and doesn’t change no matter where the adapter goes.

When an adapter wants to send a frame to some destination adapter, the sending adapter inserts the destination adapter’s MAC address into the frame and then sends the frame into the LAN.
When an adapter receives a frame, it will check to see whether the destination MAC address in the frame matches its own MAC address.
If there is a match, the adapter extracts the enclosed datagram and passes the datagram up the protocol stack.
If not, the adapter discards the frame.
Sometimes, a sending adapter want all the other adapters on the LAN to receive and process the frame it is about to send. 
In this case, the sending adapter inserts a special MAC **broadcast address**: FF-FF-FF-FF-FF-FF into the destination address field of the frame.

### Address Resolution Protocol (ARP)

The job of the **Address Resolution Protocol (ARP)** is to translate between IP addresses and MAC addresses.
For this, each host and router has an **ARP table** in it's memory, which contains mappings of IP addresses to MAC addresses.
The ARP table also contains a time-to-live (TTL) value, which indicates when each mapping will be deleted from the table.
Note that a table does not necessarily contain an entry for every host and router on the subnet; some may have never been entered into the table, and others may have expired.
If a host does not contain in it's ARP table the mapping for a particular IP, it sends an **ARP packet** to all other hosts and routers on the subnet, querying them for the mapping of the IP address required.

Note that no configuration from a network manager is required for the ARP protocol.
When a host joins the subnet, it's MAC address will eventually (if needed) reach the other node's ARP tables, as they query for it.
After a host leaves the network, it's MAC address will eventually expire from the other node's ARP tables, due to the TTL.

### Sending a Datagram off the Subnet

When a host wants to communicate with host outside it's subnet, it does the following:
1. Create an IP datagram with it's source IP and the destination's destination IP;
2. Realise that the destination is outside the subnet, using the subnet's mask;
3. Determine the router it should send the datagram to, using a network-layer protocol;
4. Find out that router's MAC address, using ARP;
5. Encapsulate the datagram in a link-layer frame with that router's MAC address as the destination MAC address.

Any router along the way will do the following:
1. Receive the link-layer frame and extract the datagram;
2. Analyze the IP on the datagram and determine where to route the datagram using a network-layer protocol;
3. Encapsulate the datagram in a link-layer frame with that node's MAC address as the destination MAC address.

The destination host will just receive the link-layer frame, extract the datagram, understand that the message has reached it's destination, and send the payload to the upper layers.

## Error Detection and Error Correction

We examine three techniques for detecting errors in the transmitted data.

### Parity Checks

Sender adds a **parity bit** which can be calculated by xoring every bit in the message.
The parity bit implies that the message (together with the parity bit) should always be even (or odd, implementation choice).  
The receiver needs only to check if the parity of the message (xoring all bits) is 0.
Parity bit error detection can only detect an even number of bit errors.
It is resilient enough for situations where bit errors are unlikely, meaning that the probability of multiple errors occurring in the same packet would be very small.
However, it has been observed that frequently, errors occur in "bursts".

One could generalize parity check by organizing the packet's bits into a grid and performing a parity check for each line and column.
With this system, when an error occurs on a bit in the grid, both the corresponding line and column parity bits will be wrong, allowing not only error detection but also error correction.
Two-dimensional parity can also detect (but not correct!) any combination of two errors in a packet.

The ability of the receiver to both detect and correct errors is known as **forward error correction (FEC)**.

### Checksumming Methods

In checksumming techniques, the bits of the packet are treated as a sequence of $k$-bit integers and added together to obtain the error-detection bits.
Checksumming methods require relatively little packet overhead, but they provide relatively weak protection against errors as compared with cyclic redundancy check.

### Cyclic Redundancy Checks

An error-detection technique used widely in today’s computer networks is based on **cyclic redundancy check (CRC) codes**, also known as **polynomial codes**.
CRC codes operate as follows:
- The sender and destination must agree on a $r+1$ bit pattern $G$, known as a **generator**, with a leading 1. Standards are set for 8-, 12-, 16-, and 32-bit generators.
- The sender must find a $r$ bit value $R$ such that the data $D$, with $R$ appended to it, divides $G$. The value $R$ can be computed through the following operation:
$$
R = D \times 2^r (\text{mod } G)
$$
- To check if the message is correct, the receiver need only check if $G$ divides $DR$.

CRC codes can easily be implemented on hardware.
That, together with their increased robustness when compared with the previous two methods, make them the most widely used of the three in link-layer protocols.  
Checksumming methods are more often used on higher layers since the probability of errors is lower and software efficiency is paramount at those layers.

## Multiple Access Protocols

There are two types of network links:
- A **point-to-point** link consists of a single sender at one end of the link and a single receiver at the other end of the link.
- A **broadcast link**, can have multiple sending and receiving nodes all connected to the same, single, shared broadcast channel.

The **multiple access problem** asks how to coordinate the access of multiple sending and receiving nodes to a shared broadcast channel.
**Multiple access protocols** present solutions on how nodes can regulate their transmissions into the shared broadcast channel.

Ideally, a multiple access protocol for a broadcast channel of rate $R$ bits per second should have the following desirable characteristics:
1. When only one node has data to send, that node has a throughput of $R$ bps.
2. When $M$ nodes have data to send, each of these nodes has a throughput of $R/M$ bps. This need not necessarily imply that each of the $M$ nodes always has an instantaneous rate of $R/M$, but rather that each node should have an average transmission rate of $R/M$ over some suitably defined interval of time.
3. The protocol is decentralized; that is, there is no master node that represents a single point of failure for the network.
4. The protocol is simple, so that it is inexpensive to implement.

### Channel Partitioning Protocols

As the name leads to believe, **channel partitioning protocols** work by partitioning the broadcast link, assigning one of the partitions to each of the participants.
This is appealing because it eliminates collisions and is perfectly fair: Each node gets a dedicated transmission rate of $R/N$ bps during each frame time. 
However, it has a major drawback: a node is limited to an average rate of $R/N$ bps even when it is the only node with packets to send.

We mention three channel partitioning protocols:
- **Time Division Multiple Access (TDMA)**: the partitioning is made in the time each node is allowed to transmit messages. TDMA divides time into **frames**, which are subdivided into **slots**. Each transmitter is assigned a slot per frame.
- **Frequency Division Multiple Access (FDMA)**: the partitioning is made in the frequency each node is allowed to transmit messages in.
- **Code Division Multiple Access (CDMA)**: each node is assigned a nod, which is then used by the nodes to encode the data bits they send. If the codes are chosen carefully, CDMA networks have the wonderful property that different nodes can transmit simultaneously and yet have their respective receivers correctly receive a send- er’s encoded data bits in spite of interfering transmissions by other nodes.

### Random Access Protocols

The second broad class of multiple access protocols are random access protocols.
In a random access protocol, a transmitting node always transmits at the full rate of the channel, namely, $R$ bps.
When there is a collision, each node involved in the collision repeatedly retransmits its frame after a random amount of time until its frame gets through without a collision.
Because the random delays are independently chosen, it is possible that one of the nodes will pick a delay that is sufficiently less than the delays of the other colliding nodes and will therefore be able to sneak its frame into the channel without a collision.

#### Slotted ALOHA

In our description of slotted ALOHA, we assume the following:
- All frames consist of exactly $L$ bits.
- Time is divided into slots of size $L/R$ seconds (that is, a slot equals the time to transmit one frame).
- Nodes start to transmit frames only at the beginnings of slots.
- The nodes are synchronized so that each node knows when the slots begin.
- If two or more frames collide in a slot, then all the nodes detect the collision event before the slot ends.

Let $p$ be a probability. The operation of slotted ALOHA in each node is simple:
- When the node has a fresh frame to send, it waits until the beginning of the next slot and transmits the entire frame in the slot.
- If there isn’t a collision, the node has successfully transmitted its frame. 
- If there is a collision, the node detects the collision before the end of the slot. The node retransmits its frame in each subsequent slot with probability p until the frame is transmitted without a collision.

Slotted ALOHA, though simple, has a few disadvantages.
When there are multiple active nodes, a certain fraction of the slots will either have collisions or be empty (no node transmits in that slot).
The slots in which exactly one node transmits is said to be a **successful slot**.
The **efficiency** of a slotted multiple access protocol is defined to be the long-run fraction of successful slots in the case when there are a large number of active nodes, each always having a large number of frames to send.
For a slotted ALOHA protocol, we can calculate the efficiency to be, as the number of nodes approaches infinity $\frac{1}{e}$, which is approximately 37%.

#### ALOHA

The slotted ALOHA protocol required that all nodes synchronize their transmissions to start at the beginning of a slot.
The first ALOHA protocol was actually an unslotted, fully decentralized protocol.
In pure ALOHA, when a frame first arrives , the node immediately transmits the frame in its entirety into the broadcast channel.
If a transmitted frame experiences a collision, the node will then immediately retransmit the frame with probability $p$.
Otherwise, the node waits for a frame transmission time.
After this wait, it then transmits the frame with probability $p$, or waits (remaining idle) for another frame time with probability $1–p$.

Using the same assumptions as the slotted case, the maximum efficiency for pure ALOHA can be found to be only $\frac{1}{2e}$, exactly half that of the slotted ALOHA.

#### Carrier Sense Multiple Access (CSMA)

Carrier Sense Multiple Access (CSMA) and CSMA with collision detection (CSMA/CD) protocols embody two rules:
- **Carrier Sensing**: a node listens to the channel before transmitting. If a frame from another node is currently being transmitted into the channel, a node then waits until it detects no transmissions for a short amount of time and then begins transmission.
- **Collision Detection**: a transmitting node listens to the channel while it is transmitting. If it detects that another node is transmitting an interfering frame, it stops transmitting and waits a random amount of time before repeating the sense-and-transmit-when-idle cycle.

The end-to-end **channel propagation delay** of a broadcast channel - the time it takes for a signal to propagate from one of the nodes to another - will play a crucial role in determining its performance.

**Carrier Sense Multiple Access with Collision Detection (CSMA/CD)**

// TODO

### Taking-Turns Protocols

#### Polling Protocols

The **polling protocol** requires one of the nodes to be designated as a master node, who polls each of the nodes in a round-robin fashion.  
Polling protocols solve the problem of collisions and wasted channels.
However, it does so at the cost of having a central node.
This introduces polling delays, meaning that no node will ever transmit at a $R$ bps rate.
More significantly, having a central node introduces an unique point of failure.

#### Token-Passing Protocol

In **token-passing protocols** a small, special-purpose frame known as a token is exchanged among the nodes in some fixed order.
When a node receives a token, it holds onto the token only if it has some frames to transmit and sends up to a maximum number of frames to the channel.
Otherwise, it immediately forwards the token to the next node.
Token passing is decentralized and highly efficient.  
However, if a failure occurs on some node, some recovery process must be launched by the remaining nodes.

## Ethernet

Throughout the 1990s, Ethernet LAN's used a coaxial bus to interconnect the nodes.  
Ethernet with a bus topology is a broadcast LAN - all transmitted frames travel to and are processed by all adapters connected to the bus.
By the late 1990s, a hub-based star topology started prevailing.
In such an installation the hosts (and routers) are directly connected to a hub with twisted-pair copper wire.
A **hub** is a physical-layer device that acts on individual bits rather than frames.
When a bit, representing a zero or a one, arrives from one interface, the hub simply re-creates the bit, boosts its energy strength, and transmits the bit onto all the other interfaces.
Thus, Ethernet with a hub-based star topology is also a broadcast LAN.  
In the early 2000s the hub at the center of this topology was replaced with a **switch**.

The Ethernet frame has the following fields:
- **Data field** (16 to 15000 bytes): carries the IP datagram. 
- **Destination address** (6 bytes): contains the MAC address of the destination adapter.
- **Source address** (6 bytes): contains the MAC address of the adapter that transmits the frame onto the LAN.
- **Type field** (2 bytes): The type field permits Ethernet to multiplex network-layer protocols.
- **Cyclic redundancy check (CRC)** (4 bytes): allows error detection.
- **Preamble** (8 bytes): Each of the first 7 bytes of the preamble has a value of 10101010; the last byte is 10101011. The first 7 bytes of the preamble serve to “wake up” the receiving adapters and to synchronize their clocks to that of the sender’s clock.

All of the Ethernet technologies provide unreliable and connectionless service to the network layer.
It uses the CSMA/CD multiple access protocol with exponential binary backoff.

It is worth noting that Ethernet is not a single protocol standard but rather a set of technologies that come in many flavors.

## Link-Layer Switches

The role of the **switch** is to receive incoming link-layer frames and forward them onto outgoing links.
The switch does this in a **transparent** way - the sender and receiver of a message are always unaware that it is intercepted by a switch.  
Switches have a forwarding table whose entries contain:
- a MAC address;
- the switch interface that leads towards that MAC address;
- the time at which the entry was placed in the table.

Whenever it receives a packet with a certain destination MAC address and from the interface $x$, it makes the following decision:
- If there is no entry in the table with the given address, the switch broadcasts a copy of the frame through all it's interfaces, except $x$;
- If there is an entry with the given address, the switch forwards the frame through the corresponding interface, except if that interface is $x$, in which case the switch discards the frame.

The forwarding table is built automatically, dynamically, and autonomously.
In other words, switches are **self-learning**.
This capability is accomplished as follows:
- The switch table is initially empty.
- For each incoming frame received on an interface, the switch stores in its table (1) the MAC address in the frame’s source address field, (2) the interface from which the frame arrived, and (3) the current time.
- The switch deletes an address in the table if no frames are received with that address as the source address after some period of time (the **aging time**).

### Switches vs. Routers

Switches:
- pros:
  - plug-and-play;
  - high forwarding rate, since they only need to process frames up to layer 2;
- cons:
  - topology restricted to spanning tree, in order to prevent cycling of frames;
  - a large switched network would require large ARP tables and generate substantial ARP traffic and processing;
  - susceptible to broadcast storms.

Routers:
- pros:
  - because network addressing is often hierarchical, packets do not normally cycle through routers even when the network has redundant paths;
  - provide firewall protection against layer-2 broadcast storms.
- cons:
  - are not plug-and-play;
  - have a larger per-packet processing time than switches.

Switches suffice for small networks, as they localize traffic and increase aggregate throughput without requiring any configuration of IP addresses.
But larger networks consisting of thousands of hosts typically include routers within the network, as they provide a more robust isolation of traffic, control broadcast storms, and use more “intelligent” routes among the hosts in the network.

## Virtual Local Area Networks (VLANs)

Switched LANs have some drawbacks:
- **Lack of traffic isolation**;
- **Inefficient use of switches**;
- **Managing users**.

These problems are solved by using a **Virtual local area network (VLAN)**.
VLANs allow multiple virtual local area networks to be defined over a single physical local area network infrastructure.
In a port-based VLAN, the switch’s ports (interfaces) are divided into groups by the network manager.
Each group constitutes a VLAN, with the ports in each VLAN forming a broadcast domain

A VLAN can span several physical switches as long as they are connected by **trunk links**.
In networks with a **VLAN trunking** solution, a special port on each switch is configured as a trunk port to interconnect VLAN switches.
The trunk port belongs to all VLANs, and frames sent to any VLAN are forwarded over the trunk link to the other switch.
In order to allow a switch to know the VLAN a frame comes from, the IEEE has defined an extended Ethernet frame format, 802.1Q, for frames crossing a VLAN trunk.
The 802.1Q frame consists of the standard Ethernet frame with a four-byte **VLAN tag** added into the header that carries the identity of the VLAN to which the frame belongs.
The VLAN tag itself consists of:
- a 2-byte Tag Protocol Identifier (TPID) field;
- a 2-byte Tag Control Information field that contains a 12-bit VLAN identifier field, and a 3-bit priority field.

![Original Ethernet frame (top), 802.1Q-tagged Ethernet VLAN frame (below)](./figs/ethernet_frame.png)

### Spanning Tree Protocols

Networks often introduce redundant links between switches to overcome the failure or congestion of links.
These connections, however, introduce physical loops into the network.
These loops are problematic since switches flood traffic out all ports when the destination is unknown.
Without any mechanism, these frames will loop forever.

This is solved by allowing physical loops, but creating loop free logical topology, through a **spanning-tree protocol**.
The Spanning-Tree Protocol establishes a root node, called the **root bridge**.
Furthermore, every node (in this context we refer to nodes as **bridges**) as unique 8 byte **bridge ID**.
For each bridge, there is **root port** which is responsible for the reception/transmission of frames from/to the root bridge.
Similarly, we define a **designated bridge** and **designated port** as the bridge and port (respectively) that are responsible for sending frames from a LAN to the root bridge and vice-versa).
Each bridge has an associated **Root Path Cost**, equal to the sum of the costs from the ports that transmit frames towards the root bridge in the least cost path to the root bridge.
The root port (for a bridge) and the designated port (for a LAN) are the ports that provide the best path to the root.
The **active ports** in a bridge are the root port and the designated ports.
The remaining ports stay inactive (blocked).

The Spanning Tree Protocol requires network devices to exchange messages to detect bridging loops.
The message that a switch/bridge sends, allowing the formation of a loop free logical topology, is called a **Bridge Protocol Data Unit (BPDU)**.
This ensures that if an active path or device fails, a new spanning tree can be calculated.

// TODO
