#Datennetze #Port 


-> Teil einer **netzwerk-Adresse**, der die Zuordnung von [[TCP]]- bzw. [[UDP]]-Verbindungen zu [[Socket|Sockets]] durch das Betriebssystem ermöglicht.

Gültige Portnummern sind **0 - 65535**!
Sie müssen **eindeutig** in dem jeweiligen Adressraum sein (TCP und UDP respektive).

Eine TCP- bzw. UDP-Verbindung wird durch das **Quadrupel** <mark style="background: #FFB8EBA6;">(Quell-IP, Quell-Port, Ziel-IP, Ziel-Port)</mark> **eindeutig** bestimmt.

Traditionell sind bestimmten Netzwerkdiensten bestimmte Portnummern zugewiesen. So ist **Port 80** etwa für Webserver und **Port 25** für SMTP-Server reserviert.

___


## Netzwerkschnittstelle, IP oder Port?

Jeder Socket hat eine eindeutige Portnummer. Der **Client** (links) will sich mit einem **Webserver** (rechts) via der [[4. Schicht -> Transportschicht]] verbinden. Die Transportschicht dient zum **Austausch von Datenpaketen zwischen den Netzwerkschnittstellen.** Um diese zu adressieren, verwendet man eine [[IP]]. Auf den kommunizierenden Computern können unterschiedliche Anwendungen laufen, welche [[Socket|Sockets]] verwenden, die durch die **Portnummer** eindeutig identifiziert werden.


![[zzDrawing_Netzwerkschnittstellen_und_Ports.png]]

Hier zu sehen: Socket mit dem Port <mark style="background: #FFB86CA6;">563</mark> möchte ein Datenpaket an den gegenüberliegenden Server schicken. 

Dazu hängt die dazwischenliegende [[4. Schicht -> Transportschicht]] einen **Header**, welcher die **Portnummer** beinhaltet, vorne an das Datenpaket. 

Dieses wird dann an die  [[Vermittlungsschicht]] übergeben, welche [[IP|IP-Adressen]] zum Zwecke des Routings verwendet. Eben diese IPs wird in den Header geschrieben -> Kombination aus IP und Port von Absender und Empfänger bilden eine **eindeutige Verbindung**.

Dann empfängt die Netzwerkschnittstelle des Empfängers das Paket, leitet es an die [[4. Schicht -> Transportschicht]] weiter, welche den Header ausließt und die Daten zum entsprechenden Port weitergibt.

***Also: 
IPs dienen zur Identifizierung von Netzwerkschnittstellen, 
Portnummern zur Identifizierung der einzelnen Sockets!***

____

