

```
io.on('connection', (socket) => {
    console.log("New WebSocket Connection");
    socket.emit('message', 'Welcome!');
});
```

Sends to particular connected client
`socket.emit('countUpdated', count);`

Sends to every single connected client
`io.emit('countUpdated', count);`
