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

## OUTPUT:
SERVER CODE: echo-server.py:

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

CLIENT CODE: echo-client.py:

import socket
HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")
## RESULT:
Server Output:
![Screenshot 2024-03-05 212505](https://github.com/manikandan26052004/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/d328014a-00fb-4a80-8b45-890f6c26c9ec)

Client output:

![hat1](https://github.com/manikandan26052004/Ethicka-Hacking-Techniques---19CS417-/assets/121999845/70849014-6563-4cb0-8a67-b47df3c71ebd)


The program is executed successfully
