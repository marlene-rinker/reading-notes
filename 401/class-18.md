## Code 401 Reading Assignment Notes - Class 18

_July 1, 2020_

[Socket.io](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-18/DISCUSSION)



#### Web Sockets

A communication Protocol which provides bidirectional communication between the Client and the Server over a TCP connection, WebSocket remains open all the time so they allow the real-time data transfer. When clients trigger the request to the Server it does not close the connection on receiving the response, it rather persists and waits for Client or server to terminate the request.

#### Socket.io

It is a library which enables real-time and full duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. 

Generally, it is divided into two parts, each of which use WebSockets, but also provide additional functionality such as broadcasting, namespacing, and other means of segmenting connected clients into groups.

  - Client Side: it is the library that runs inside the browser

  - Server Side: It is the library for Node.js

#### Connections

With TCP, you connect directly to a server with a keep-alive type of connection.

With Socket.io, you connect to a server over HTTP. The session is “kept alive” through it’s internal use of the WebSocket Protocol, with session information being preserved.

#### Messaging

Standard node events are sent with `emit()` and received with `on()` … Socket.io uses the same methodology/terminology.

With Socket.io, the entire purpose is to have events shared between ‘disconnected’ participants. Through a mediator (server), clients connect, emit events, and respond to events from the server.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-18/DISCUSSION) has an example of a typical flow.

_**Not every client will have a listener for every event.**_

_**The server may not have a listener for every event the client sends.**_



#### Additional Resources

[WebSockets - wikipedia](https://en.wikipedia.org/wiki/WebSocket)

[Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)

[WebSocket vs Socket.io](https://www.educba.com/websocket-vs-socket-io/)

[Socket.io documentation](https://socket.io/docs/)

[Socket.io docs - server API](https://socket.io/docs/server-api)

[Socket.io docs - client API](https://socket.io/docs/client-api)

[Socket.io Testing Tool](https://amritb.github.io/socketio-client-tool/)







---
[Home page](https://marlene-rinker.github.io/reading-notes/)