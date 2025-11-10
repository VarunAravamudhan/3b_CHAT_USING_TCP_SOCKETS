# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Server
~~~
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
~~~
### Client
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~

## OUPUT
### Server

<img width="1275" height="272" alt="image" src="https://github.com/user-attachments/assets/ca3478a0-4907-4b2f-a2f9-beb66eea6121" />

### Client

<img width="1168" height="249" alt="image" src="https://github.com/user-attachments/assets/eb20dbfd-7e13-41eb-bf79-3e9e307e7e35" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
