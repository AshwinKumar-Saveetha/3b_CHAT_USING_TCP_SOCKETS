# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Ashwin Kumar A
## REG NO:212223040021
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER
```python
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
### CLIENT
![image](https://github.com/AshwinKumar-Saveetha/3b_CHAT_USING_TCP_SOCKETS/assets/155129814/fedff861-c9bf-4aae-b8f7-1334834d2b52)

### SERVER
![image](https://github.com/AshwinKumar-Saveetha/3b_CHAT_USING_TCP_SOCKETS/assets/155129814/5ac75116-6585-4770-8b12-c30259b5ecd0)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
