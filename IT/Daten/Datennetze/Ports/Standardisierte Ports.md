#Datennetze #Port 

## Drei Port-Bereiche:

### System Ports#
-> Auch: **Well-Known Ports**! 
<mark style="background: #D2B3FFA6;">Ports 0 - 1024</mark>
Sie sind ausschließlich für IANA standardisierte Dienste bzw. Protokolle vorgesehen. Auf Unix-artigen Betriebssystemen werden oftmals **Root-Rechte** vorausgesetzt, um diese Ports verwenden zu können.

### User Ports
<mark style="background: #D2B3FFA6;">Ports 1024 - 49151</mark>
Können von Server-Diensten, als auch von Client-Programmen verwendet werden. 
Keine **dynamische Zuordnung** zu [[Client-Socket|Client-Sockets]]! -> Normaler Weise übernimmt das Betriebssystem die Zuordnung automatisch.

### Dynamic Ports
<mark style="background: #D2B3FFA6;">Ports 49152 - 65535</mark>
Diese Ports werden vom Betriebssystem dynamisch an [[Client-Socket|Client-Sockets]] vergeben.
Nicht alle Betriebssysteme halten sich aber an diesen Standard!



