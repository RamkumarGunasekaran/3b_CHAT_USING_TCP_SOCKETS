## NAME: RAMKUMAR G
## REG NO: 212223220084
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
## client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## server
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
## OUPUT
## client
![Screenshot 2024-10-24 111450](https://github.com/user-attachments/assets/ae789a95-b7f7-45b8-a288-de36faa52662)
## server
![Screenshot 2024-10-24 111502](https://github.com/user-attachments/assets/3ee0131d-bbc0-4119-be23-50ea3fb26f8c)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
