# 4a.WRITE A CODE SIMULATING PING COMMAND
```
NAME:RAGUNATH R
REG NO:212222240081
```
# AIM
To write the python program for simulating ping command.Sockets Links.
## ALGORITHM:
Step 1: start the program.
Step 2: Include necessary package in java.
Step 3: To create a process object p to implement the ping command. Step 4: declare one Buffered Reader stream class object.
Step 5: Get the details of the server 5:1: length of the IP address.
     5:2: time required to get the details.
     5:3: send packets, receive packets and lost packets.
     5.4: minimum, maximum and average times.
Step 6: print the results.
Step 7: Stop the program.
## PROGRAM:
## CLIENT:
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost'8000))
s.listen(5)
c,addr=s.accept()
while True:
   hostname=c.recv(1024).decode()
   try:
     c.send(str(ping(hostname, verbose=False)).encode())
   except KeyError:
     c.send("Not Found".encode())
```
## SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   ip=input("Enter the website you want to ping ")
   s.send(ip.encode())
   print(s.recv(1024).decode())

```
## OUPUT:
## CLIENT:
![image](https://github.com/Ragu-123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113915622/0b816d90-bb7d-4f47-ba73-c64ab3343c50)
## SERVER:
![image](https://github.com/Ragu-123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113915622/f63efc0e-ac30-4d84-b467-1fcc39714fa5)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
