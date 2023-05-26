# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE :27-04-2023

## AIM :To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


## ALGORITHM :
1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server.

4.Send and receive the message using the send function in socket.

## PROGRAM :
## CLIENT:
```
Developed by: P SYAM TEJ
Register No: 212221240056
```
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~
## SERVER:
~~~
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
~~~

## OUTPUT :
## CLIENT:
![image](https://github.com/NAGINENIROHITH/EX-8/assets/118344049/36aba797-badd-46a0-be3e-f1b63d7dc5fc)

## SERVER:
![image](https://github.com/NAGINENIROHITH/EX-8/assets/118344049/c1c0a831-0e0e-4553-8f2f-8826750bd6c6)


## RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
