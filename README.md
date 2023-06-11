# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:DATE: 16-03-2023

# AIM :
To write a python program to perform stop and wait protocol.
# ALGORITHM :
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK 
   signal to client.
6. Stop the program

# PROGRAM :
```
Developed By: G.Jayanth.
Reg. No.: 212221230030
```
```
# client

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
        
   # server
   ```
   import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())

# OUTPUT :
Client Side:
![image](https://github.com/JayanthYadav123/EX-2/assets/94836154/0613d3ca-d6fc-4b2d-a6fd-1222d9924e2a)
Server Side:
![image](https://github.com/JayanthYadav123/EX-2/assets/94836154/9dce6d1e-2bb0-48b0-b082-91017c3eaf0a)
# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.





