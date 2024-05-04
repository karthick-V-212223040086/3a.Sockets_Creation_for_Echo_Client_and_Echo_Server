# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT:
## CLIENT:

![image](https://github.com/karthick-V-212223040086/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037461/2490ebc5-9b4a-4167-aa44-4c4fe0d74b54)

## SERVER:
![image](https://github.com/karthick-V-212223040086/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149037461/b735966e-bd31-4173-b83c-6942efcc04f4)
## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
