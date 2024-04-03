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
```
CLIENT :
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

SERVER :
 
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
CLIENT :
![Screenshot 2024-04-03 154951](https://github.com/NaliniG007/3b_CHAT_USING_TCP_SOCKETS/assets/144870858/415255dc-5823-4021-a387-c5ac729486f3)

SERVER :
![Screenshot 2024-04-03 155003](https://github.com/NaliniG007/3b_CHAT_USING_TCP_SOCKETS/assets/144870858/68d7879c-c1d3-4c8f-b6b0-a2d8cd9f3033)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
