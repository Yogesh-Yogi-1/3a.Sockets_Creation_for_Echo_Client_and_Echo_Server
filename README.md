# EX NO 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME: V.YOGESH
## REG NO : 212223230250
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT
![Screenshot 2024-05-15 213135](https://github.com/Yogesh-Yogi-1/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148514598/464bff02-ef50-46b2-92c2-f9c382a8c621)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links `
