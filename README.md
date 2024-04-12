# 2a_Stop_and_Wait_Protocol
Reg no:212223240024\
Name:Deepika P
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAMT
CLIENT:
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
    s.send("Acknowledgement Recived".encode())
## OUTPUT
CLIENT:![Screenshot 2024-04-11 220551](https://github.com/deepicqqq/2a_Stop_and_Wait_Protocol/assets/162718406/41045b9f-6c5d-43ec-a243-dc229f887cfe)
SERVER:![Screenshot 2024-04-11 220643](https://github.com/deepicqqq/2a_Stop_and_Wait_Protocol/assets/162718406/8e76cce2-4afa-4a00-b4a5-2d6bce2135c0)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
