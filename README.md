`# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# NAME: yogesh.v

# REGISTER NO: 212223230250
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
CLIENT
```
import socket

HOST = '127.0.0.1'  
PORT = 65432        

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    while True:
        message = input("Enter message to send to server: ")
        s.sendall(message.encode())
        data = s.recv(1024)
        print('Received', repr(data.decode()))
```
SERVER
```
import socket

HOST = '127.0.0.1'  
PORT = 65432       

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print('Connected by', addr)
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
## OUPUT
CLIENT
![328375958-8e12ef30-b330-46d6-a024-40af188711b0](https://github.com/Yogesh-Yogi-1/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148514598/a62028b6-3301-4dc5-a239-d5c0fe242e5b)


SERVER
![328376017-d23b1011-d18a-4adf-bca7-fd4f4ff47315](https://github.com/Yogesh-Yogi-1/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148514598/275e41fa-5f7f-4f83-a1ad-bd268b2cb103)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links `
