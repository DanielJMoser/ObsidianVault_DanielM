#Datennetze 

-> **Transmission Control Protocol**
-> Ein [[Zuverlässigkeit & Verbindungsorientiertheit#Zuverlässigkeit:|zuverlässiges]], [[Zuverlässigkeit & Verbindungsorientiertheit#Verbindungsorientiertheit:|verbindungsorientiertes]] Protokoll.

Die darunterliegenden Schichten sind aber immer noch **unzuverlässig**!

- Datenpakete können aus der Reihung ankommen,
- verloren gehen,
- oder korrumpiert werden!

Um einen **zuverlässigen Transport** zu garantieren, muss TCP zusätzliche Maßnahmen implementieren:

- Sequenznummern
  - Durchnummerierung, um Reihenfolge sicherzustellen
- [[ARQ-Protokolle|Retransmission / Automatic Repeat Request]]
  - Verloren gegangene Pakete werden vorerst einfach ausgelassen.
- Checksummen
  - ...um festzustellen, ob Pakete korrumpiert wurden.

____

## Header

![[zzDrawing_TCP_header.png]]

**Variable Größe!** -> immer ein Vielfaches von 4 Byte. 
Minimale Größe: 20 Byte
Maximale Größ: 60 Byte


### Data Offset

Start der Nutzdaten wird durch dieses Feld angegeben. Es ist selbst **4 Bit** groß und gibt die Größe des Headers in **4-Byte-Wörtern** an.

Das Data Offset **multipliziert mit 4 Byte** ergibt den tatsächlichen Offset.


### Größe der Nutzdaten

-> In diesem Header ist **kein** Feld für die Größe der Nutzdaten vorgesehen!
Im **IP-Header** allerdings steht die **Größe des Gesamtpakets**. 
Zählt man davon nun <mark style="background: #D2B3FFA6;">IP-Header</mark> und <mark style="background: #D2B3FFA6;">TCP-Header</mark> ab, so erhält man die Größe der Nutzdaten.


### Sequenznummern

Die Sequenznummern nummerieren die **Bytes im Datenstrom**.

![[zzDrawing_Sequenznummern]]


Im TCP-Header steht die Sequenznummer des **ersten Byte** der Nutzdaten. Die Anfangssequenznummer kann dabei frei gewählt werden.

Durch **aufsteigendes Sortieren** kann die Reihenfolge der Datenpakete ermittelt werden. Anhand der Sequenznummer und Größe der Nutzdaten werden **Lücken** im Datstrom erkannt:

<mark style="background: #D2B3FFA6;">Paket 1</mark> hat die Sequenznummer 100. Größe der Nutzdaten ist 50.
<mark style="background: #FFB8EBA6;">Paket 2</mark> hat die Sequenznummer 200.

-> Es gibt eine Lücke von 50 Bytes zwischen <mark style="background: #D2B3FFA6;">P1</mark> und <mark style="background: #FFB8EBA6;">P2</mark>. Das obige <mark style="background: #FFB8EBA6;">Paket 2</mark> ist eigentlich das <mark style="background: #BBFABBA6;">Paket 3</mark>! <mark style="background: #FFB8EBA6;">P2</mark> ging unterwegs verloren.

___

### Garantie eines zuverlässigen Datentransports

Da die darunterliegenden Schichten unzuverlässig sind, passiert das immer wieder. Ein zuverlässigen Datentransport kann durch [[ARQ-Protokolle]] gewährleistet werden. TCP verwendet dabei das [[ARQ-Protokolle#Go-back-N|Go-back-N-Verfahren]].

[[ARQ-Protokolle#^a2f277|Retransmission Timeout]] wird ständig **dynamisch** an die konkreten Gegebenheiten angepasst. Dazu wird die **Rount-Trip-Time** gemessen und anhand derer die RTO neu berechnet.
Ebenso: -> **Fenstergröße**

Um Datenpakete zu bestätigen, sendet der Empfänger ein Paket, in dessen TCP-Header die Sequenznummer des **nächsten erwarteten Pakets** enthalten ist.
- Falls keine zu sendende Daten -> **leeres Paket**

TCP kennt auch **negative Bestätigungen**. Dazu wird die Bestätigung des **vorherigen** Pakets nocheinmal gesendet. Empfängt der Sender ein Paket mehrfach (sog. **DUP-ACK**), so muss er das nachfolgende Paket nocheinmal senden.
