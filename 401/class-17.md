## Code 401 Reading Assignment Notes - Class 17

_June 30, 2020_

[TCP Servers](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-17/DISCUSSION)

### TCP Servers

#### Event Queues

Much of the NodeJS architecture is built around the use of events. All objects that emit events in NodeJS are instances of the EventEmitter constructor. EventEmitter’s are a great way to handle controlling asynchronous events. Functions can be registered as listeners for an event on instances of the EventEmitter class. These instances can emit events and pass the listener’s data.

In practical applications, multiple “disconnected” services can communicate with one another using various protocols using proprietary APIs. Generally, this is done through a central “Hub” server (or Queue) which receives all inbound messages, scrubs the content, and then broadcasts those messages to connected subscribers.

#### OSI Model

In the mid 1980s the “Open Systems Interconnection Reference Model” (OSI model) was developed as a seven layer model. This seven layer OSI model has continued to accurately describe the different processes in computer networking, and is still widely used as a point of reference while working in networked systems today. A developer or engineer is usually responsible for the goals of a specific layer and communicating with the layer above and below. Not every computer network solution uses all seven layers, for example HTTP skips the Presentation and Session layers and lives directly on top of the Transport layer.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-17/DISCUSSION) contains descriptions and examples of each layer.

#### Internet Protocol Suite

The Internet Protocol Suite is the conceptual model for the protocols used by the internet. It is often referred to as TCP/IP because the IP and TCP were the original protocols in the suite. The Internet Protocol Suite is described using four layers - Link, Internet, Transport, and Application. Web developers often reference the Internet Protocol Suite model when discussing network communication and data exchange.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-17/DISCUSSION) contains descriptions and examples of each layer.

**_TCP_**

TCP creates a two way communication between two hosts and provides reliable, ordered, and error checked byte streams between the applications.

Each IP packet between the hosts carries a single TCP Segment. A TCP segment is made up of header and data sections.

The TCP Header is used at each end to control the type of interaction being sent. [Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-17/DISCUSSION) contains a good description of the information that's included in the header.

#### Connection Establishment

The client sends a SYN packet with an random initial sequence number. The server sends a SYN-ACK packet with the acknowledgment number set to one more than the initial sequence number. The client responds with an ACK and an acknowledgment number incremented by one.

#### Connection Termination

One end sends a FIN Segment and the other sends an ACK segment followed by a FIN segment. The termination initiation will then respond with an ACK segment.



#### Additional Resources

[OSI Model Video](https://www.youtube.com/watch?v=vv4y_uOneC0)

[TCP 3 Way Handshake Video](https://www.youtube.com/watch?v=xMtP5ZB3wSk)

[OSI Model](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/) - has extensive details about the model and each layer

[What is TCP](https://searchnetworking.techtarget.com/definition/TCP)

[Build a Simple TCP Server & Client](https://techbrij.com/node-js-tcp-server-client-promisify) - has code examples

[Node.js documentation - net module](https://nodejs.org/api/net.html)






---
[Home page](https://marlene-rinker.github.io/reading-notes/)