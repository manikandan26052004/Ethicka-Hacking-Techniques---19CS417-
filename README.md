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
![308189013-c2009444-d6c9-4fe2-b32b-1bc05adfae9c](https://github.com/IsaacAIML2023/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/57e935cc-b79d-4db4-8258-ae4a4994776a)
![308188975-c4e30dcb-f338-4d50-99a4-57881a361074](https://github.com/IsaacAIML2023/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/95dcc913-3353-48a2-a8a9-1c2e27e67828)

## RESULT:
The program is executed successfully
