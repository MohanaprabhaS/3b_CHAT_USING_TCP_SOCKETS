# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Mohanaprabha S
## Date:20.5.25
## Register no:212224040197
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
Client
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())

Server
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())

```
## OUPUT

![Screenshot 2025-05-12 161301](https://github.com/user-attachments/assets/11756b55-8ddd-4d1a-8cb2-bd57c34ef6e6)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
