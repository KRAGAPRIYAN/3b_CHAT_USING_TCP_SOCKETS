# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.

## Date: 14/02/2026
## Roll.No: 212225040323

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

server.py

```
import socket
s=socket.socket()
s.bind(('localhost',10101))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client: ",ClientMessage)
    msg=input("Server: ")
    c.send(msg.encode())
```

client.py

```
import socket
s=socket.socket()
s.connect(('localhost',10101))
while True:
    msg=input("Client: ")
    s.send(msg.encode())
    print("Server: ",s.recv(1024).decode())
```

## OUPUT

Server-Side

![alt text](<Screenshot 2026-02-14 110827.png>)

Client-Side

![alt text](<Screenshot 2026-02-14 110844.png>)

Execution

![alt text](<Screenshot 2026-02-14 110810.png>)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
