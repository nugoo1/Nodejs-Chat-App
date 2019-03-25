Socket.io

**See code for socket.io initialization with express

Following code runs on connection

```
io.on('connection', (socket) => {
    console.log("New WebSocket Connection");
    socket.emit('message', 'Welcome!');
});
```

Common Actions

Sends to particular connected client
`socket.emit` 

Sends to every single connected client
`io.emit`
`socket.broadcast.emit`

Sends to particular connected client
`socket.emit('countUpdated', count);`

`io.emit('countUpdated', count);`

Send to everyone but that client - ** .to(room) ** specifies the room to connect to
````
socket.broadcast
      .to(user.room)
      .emit("message", generateMessage("admin",`${user.username} has joined!`));

````
