# Ethicka-Hacking-Techniques---19CS417-
Ethicka Hacking Techniques - 19CS417 
# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
## OUTPUT:
![308189013-c2009444-d6c9-4fe2-b32b-1bc05adfae9c](https://github.com/IsaacAIML2023/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/3d57f36b-ae58-423c-9871-d1c1884e5563)

![308188975-c4e30dcb-f338-4d50-99a4-57881a361074](https://github.com/IsaacAIML2023/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/4a27800b-c526-4160-a4f5-134419bec8cf)


## RESULT:
The program is executed successfully
