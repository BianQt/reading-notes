# Message Queues
## Socket.io Chat
Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

This means that the server can push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.


## Rooms and Namespaces
Once you have a basic server setup, and a socket connection initialized and assigned to a variable, typically io, it’s time to start thinking about namespaces. By default, if a namespace is not specified, they will be attached to the default namespace /.
###
**Namespaces** are used to separate server logic over a single shared connection. A common use may be to separate admin concerns from those of regular users.
I recently built a video chat application that also had a text chat. In order to modularize the code I used two different namespaces.
###
**Rooms** are subdivisions of namespaces that can be created by the server. This allows you to broadcast data to a subset of related sockets.

Two useful methods are provided for joining and leaving rooms, .join(room, callback) and .leave(room, callback) respectively. Both take two parameters, the room name and a callback.

My video chat application had several rooms and users were free to switch between them. Each time a user would switch, the client would emit the previous room and the new room.

The listener on the server would start by leaving the previous room with socket.leave(). Then, within the callback, the server connects the client to the new room with socket.join().
## Socket.io Emit
All of the ```.on``` listeners should correspond to an ```.emit``` method on the client side, except the disconnect listener will run anytime a client disconnects from the server. This emit signal is sent automatically by the client.

The Socket.IO API is inspired from the Node.js EventEmitter, which means you can emit events on one side and register listeners on the other:
```
// server-side
io.on("connection", (socket) => {
  socket.emit("hello", "world");
});

// client-side
socket.on("hello", (arg) => {
  console.log(arg); // world
});
```
