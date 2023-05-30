# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE : 27-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :
1.Start the program.

2.Get the frame size from the user

3.To create the frame based on the user request.

4.To send frames to server from the client side.

5.If your frames reach the server, it will send ACK signal to client otherwise it will send NACKsignal to client.

6.Stop the program.

## PROGRAM :
## CLIENT:
## Developed By : MALARVIZHI G
## Reg no : 212222040096

import socket

s = socket.socket()

s.connect(('localhost', 8000))

while True:

    msg = input("Client > ")
    
    s.send(msg.encode())
    
    print("Server > ", s.recv(1024).decode())
## SERVER:
import socket

s = socket.socket()

s.bind(('localhost', 8000))

s.listen(5)

c, addr = s.accept()

while True:

    ClientMessage = c.recv(1024).decode()
    
    c.send(ClientMessage.encode())

    


## OUTPUT :
## CLIENT:
![EX 8 CLIENT](https://github.com/22008650/EX-8/assets/122548204/28cb314f-5893-4979-b4e1-d680d827b4de)
## SERVER:
![EX 8 SERVER](https://github.com/22008650/EX-8/assets/122548204/a60cf2e0-e4ff-44b6-b351-54a57d00ee96)


## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
