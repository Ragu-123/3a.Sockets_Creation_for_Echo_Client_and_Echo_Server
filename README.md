# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
```
NAME:RAGUNATH R
REG NO:212222240081
```
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## OUPUT:
## CLIENT:
![WhatsApp Image 2024-04-11 at 14 15 00_5a28ad07](https://github.com/23002027/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139752981/7a6579f1-6e60-45bd-b2c6-39d3e203704a)
## SERVER:
![WhatsApp Image 2024-04-11 at 14 15 15_d753fdc8](https://github.com/23002027/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139752981/ae3747b9-656f-47e6-8f9b-341ff1448b25)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
