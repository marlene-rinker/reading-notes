## Code 401 Reading Assignment Notes - Class 19

_July 2, 2020_

[Message Queues](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-19/DISCUSSION)



### Message Queues

A Queue server runs independently, and is tasked with routing events and messaging between clients.

- Any connected client can “publish” a message into the server.
- Any connected client can “subscribe” to receive messages by type.

A message is a package of information categorized by queue and event.

`queue` - which general bucket does this message belong in; for example, "Database Events", "Filesystem Events", etc.

`event` - what event has happened; for example, "delete, add, update, connection lost, error", etc.

`payload` - data associated with the event; for example, "record id, record information, error text", etc.

#### Real Time vs Queued Messaging

In some cases, messages are simply brokered by the server. They come in, are processed and are immediately broadcast out to subscribers. Should a subscriber at any point lose connection with the server, any messages broadcast by the server will clearly be missed by the client. These are known as **Real Time** messaging systems.

A true **Queue** will keep track of the delivery status of every event/message. Any broadcast that is not received by a subscriber will remain in the queue until it can be delivered. In this type of systems, rather than a broadcasting of messages, clients will likely poll the server to retrieve any messages in the queue for them, on their own timeline/schedule.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-19/DISCUSSION) has a descriptive Use Case for queued messages.


#### Additional Resources

[Rooms and Namespaces - Socket.io](https://socket.io/docs/rooms-and-namespaces/)

[Emit cheatsheet - Socket-io](https://socket.io/docs/emit-cheatsheet/)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)