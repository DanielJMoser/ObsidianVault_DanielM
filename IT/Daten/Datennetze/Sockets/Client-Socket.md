#Datennetze #Socket

## Client-Socket in Python:

```python
import socket 

# Erzeuge Stream
Socket sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM) 
# Verbinde Socket mit dem Server 192.168.0.1 Port 80 
# Für den Client-Socket selber muss kein eigener Port 
# angegeben werden, er wird vom Betriebssystem 
# automatisch zugewiesen 
sock.connect(("192.168.0.1", 80)) 
# Sende und/oder Empfange Daten 
sock.send(data) 
buffer = sock.recv(1024)

...

# Schließe Socket 
sock.close()
```

