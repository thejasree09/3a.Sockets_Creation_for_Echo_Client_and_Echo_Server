# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
#NAME:Theja sree G
##Ref no:212224110056
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
server.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
client.py
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
SERVER:

![Screenshot 2025-03-28 141833](https://github.com/user-attachments/assets/1a34ca08-f3a4-473f-bc5c-9d47864cf9ec)

CLIENT:

![Screenshot 2025-03-28 141843](https://github.com/user-attachments/assets/5e8051ff-b6b9-476c-94c2-f2f097053816)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
