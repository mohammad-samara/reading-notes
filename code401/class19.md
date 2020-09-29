# Message Queues  

 we know that the queue is a line of things waiting to be handled, starting at the beginning of the line and processing it in sequential order  
 so the **message queue** is a queue of messages sent between applications.  

- It includes a sequence of work objects that are waiting to be processed
- it allows applications to communicate by sending messages to each other  
- it provides temporary message storage when the destination program is busy or not connected.  

![msgQueue](../images/401/msgQueue.PNG)  

## What is a message

  is a package of information, categorized by :

- **queue** --> Which general bucket does this message belong for example “Database Events”, “Filesystem Events”  
- **event** --> What event has happened like “delete, add, update, connection lost, error”, etc.  
- **payload** --> data associated with the event like  “record id, record information, error text”, etc.  

## Real Time vs Queued Messaging

  messages are simply brokered by the server.  
  They come in, are processed and are immediately broadcast out to subscribers.  
  Should a subscriber at any point lose connection with the server,  
  any messages broadcast by the server will clearly be missed by the client. These are known as “Real Time” messaging systems.  

## Socket.io Namespaces

Socket.IO allows you to “namespace” your sockets, which essentially means assigning different endpoints or paths.

This is a useful feature to minimize the number of resources (TCP connections) and at the same time separate concerns within your application by introducing separation between communication channels.

### Default namespace

We call the default namespace / and it’s the one Socket.IO clients connect to by default, and the one the server listens to by default.

### Custom namespaces

To set up a custom namespace, you can call the of function on the server-side

### Rooms

Within each namespace, you can also define arbitrary channels that sockets can join and leave.

We can call join to subscribe the socket to a given channel:

`io.on('connection', function(socket){`
  `socket.join('some room')`;
`});`
And then simply use to or in (they are the same) when broadcasting or emitting:

`io.to('some room').emit('some event');`

To leave a channel you call leave in the same fashion as join. Both methods are asynchronous and accept a callback argument.
