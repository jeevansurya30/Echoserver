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
## CLIENT:
```
import socket
HOST, PORT = '172.20.10.2', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Jeevansurya, 212222040061')
    print(f'Received: {s.recv(1024)!r}')

```

## SERVER:
```
import socket
HOST, PORT = '172.20.10.2', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```

## OUTPUT:
## CLIENT:
![sever ss](https://github.com/user-attachments/assets/de89e112-67eb-45e2-bd84-b9a61f58c84d)

## SERVER:
![client ss](https://github.com/user-attachments/assets/1fa701fe-7c8a-4025-a639-5b434bbb62a7)



## RESULT:
The program is executed successfully
