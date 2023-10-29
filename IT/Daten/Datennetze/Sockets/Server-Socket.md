#Datennetze #Socket 

## Server-Socket in Python:

```python

import socket

# Erzeuge Stream Socket. Dieser ist noch unspezifiziert!
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM) 
# Binde Socket an Adresse. Ab nun ist er ein Server-Socket!
# "0.0.0.0" -> Alle verfügbaren Adressen, Port 80.
sock.bind(("0.0.0.0", 80))
# Warte auf Anfrage eines Clients.
sock.listen()

while True: 
	# Akzeptiere Anfrage des Client. 
	clientsock, addr = sock.accept() 
	# Empfange und sende Daten.
	buffer = clientsock.recv(1024) clientsock.send(data) 
	# Schließe Client-Socket.
	clientsock.close()

```

Python verwendet sog. **POSIX**-Sockets.
**sock.accept** wird üblicher Weise in einer **Endlosschleife** aufgerufen und gibt einen clientsock zurück, welcher dann für die eigentliche Kommunikation verwendet wird.