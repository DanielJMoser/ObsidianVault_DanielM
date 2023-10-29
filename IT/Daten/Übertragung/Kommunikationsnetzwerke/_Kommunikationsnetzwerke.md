# Kommunikationsnetzwerke
#embeddedsystems 
#kommunikationsnetzwerke 
#Datennetze 

-> für [[_Embedded Systems|Embedded Systems]] folgende Kriterien

* Sicherheit
* Zuverlässigkeit
* Robustheit
* [[Echtzeitsysteme|Echtzeitfähigkeit]]

Für [[_Embedded Systems|Embedded Systems]]: Zwei relevante Arten von Kommunikationsnetzwerken!

* [[Punkt-zu-Punkt Verbindung]]
* [[Bus-Systeme]]

-----------------------------

## Synchronisierung

### Synchron
Einzelne Bits werden übertragen, zeitlich durch globales **Taktsignal** synchronisiert.

### Asynchron
Kommunikationspartner*innen* arbeiten mit mehreren **Taktgebern**, die vor jeder Übertragung (oft via Startbits) synchronisiert werden müssen.

-----------------------

## Übertragung von Bits

### Seriell
Hintereinandersendung über Datenkanal. Sowohl [[_Kommunikationsnetzwerke#Synchron|synchron]] als auch [[_Kommunikationsnetzwerke#Asynchron|asynchron]] möglich.

### Paralell
Gleichzeitiges Senden über mehrere Datenkanäle. Nur [[_Kommunikationsnetzwerke#Synchron|synchron]] möglich.

---------------------------

## Kommunikationsrichtungen

### Unidirektional
Nur eine Richtung.

### Bidirektional
Beide Richtungen.

Hierbei zu unterscheiden:

#### Halbduplex
Entweder Empfangen oder Senden. -> *CB-Funk*

#### Vollduplex
Gleichzeitiges Empfangen und Senden möglich. -> *Telefonie*



---------------------

## Empfänger_innen der Nachricht

### Broadcast
An alle Teilnehmer_innen

### Unicast
An eine Teilnehmer_in

### Multicast
An eine Teilmenge >1 aller Teilnehmer_innen

---------------------------------------

