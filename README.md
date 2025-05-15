# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
# Name: Vikaash P
# Reg.No: 212223240180
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Server.py
```
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
Client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
Server
![image](https://github.com/user-attachments/assets/50918ca0-3fb7-44c8-a2ff-101d9ede3ecb)

Client
![image](https://github.com/user-attachments/assets/d9857349-0bd3-43da-aa68-2971c6b42d0f)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
