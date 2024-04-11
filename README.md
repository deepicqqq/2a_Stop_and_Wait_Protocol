# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
CLIENT:\
import socket\
s=socket.socket()\
s.bind(('localhost',8000))\
s.listen(5)\
c,addr=s.accept()\
while True:\
    i=input("Enter a data: ")\
    c.send(i.encode())\
    ack=c.recv(1024).decode()\
    if ack:\
        print(ack)\
        continue\
    else:\
        c.close()\
        break

SERVER:\
import socket\
s=socket.socket()\
s.connect(('localhost',8000))\
while True:\
    print(s.recv(1024).decode())\
    s.send("Acknowledgement Recived".encode())\
## OUTPUT
CLIENT:![Screenshot 2024-04-11 220551](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/162718406/fbd82857-3514-4ac5-9fc2-80acc26bb00e)
SERVER:![Screenshot 2024-04-11 220643](https://github.com/NaliniG007/2a_Stop_and_Wait_Protocol/assets/162718406/adf8faf4-cc42-42b5-8468-2fa1b3fa56ff)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
