# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE : 27-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :
### STEP 1: Start the program.
### STEP 2: Get the frame size from the user
### STEP 3: To create the frame based on the user request.
### STEP 4: To send frames to server from the client side.
### STEP 5: If your frames reach the server, it will send ACK signal to client otherwise it will send NACKsignal to client.
### STEP 6: Stop the program.

## PROGRAM :
## CLIENT:
## Developed By : MALARVIZHI G
## Reg no : 212222040096
```
import socket
s = socket.socket()
s.connect(('localhost', 8000))
while True:
    msg = input("Client > ")    
    s.send(msg.encode())    
    print("Server > ", s.recv(1024).decode())
```
## SERVER:
```
import socket
s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
c, addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()    
    c.send(ClientMessage.encode())
```

    


## OUTPUT :
## CLIENT:
![ex08 client output](https://github.com/22008650/EX-8/assets/122548204/1c1b4245-f3b0-47b3-a145-b2e17ef87f44)
## SERVER:
![ex08 server output](https://github.com/22008650/EX-8/assets/122548204/32f385fc-c99f-4dec-9c3d-dfe054f5bd17)

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
