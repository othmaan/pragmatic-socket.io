# pragmatic-socket.io
Curated list of solutions from stackoverflow &amp; others


// Sending to sender-client only
```javascript
 socket.emit('message', "this is a test");
```

 // Sending to all clients, include sender
 ```javascript
 io.emit('message', "this is a test");
 ```

 // Sending to all clients except sender
 ```javascript
 socket.broadcast.emit('message', "this is a test");
 ```

 // Sending to all clients in 'game' room(channel) except sender
 ```javascript
 socket.broadcast.to('game').emit('message', 'nice game');
 ```

 // Sending to all clients in 'game' room(channel), include sender
 ```javascript
 io.in('game').emit('message', 'cool game');
 ```

 // Sending to sender client, only if they are in 'game' room(channel)
 ```javascript
 socket.to('game').emit('message', 'enjoy the game');
 ```

 // Sending to all clients in namespace 'myNamespace', include sender
 ```javascript
 io.of('myNamespace').emit('message', 'gg');
 ```

 // Sending to individual socketid
 ```javascript
 socket.broadcast.to(socketid).emit('message', 'for your eyes only');
 ```
