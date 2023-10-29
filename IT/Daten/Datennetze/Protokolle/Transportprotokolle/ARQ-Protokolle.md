#Datennetze 

-> **Automatic Repeat reQuest** ^a2f277

Dabei bestätigt der Empfänger den **fehlerfreien Erhalt der Daten.**
Erhält der Sender keine solche Bestätigung -> **retransmission.**

Der Sender wartet eine bestimmte Zeitspanne **(Retransmission Timeout, RTO)** auf die Bestätigung, bevor er das Paket abermals sendet.
Das Datenpaket wird nun so oft neu übertragen, bis es beim Empfänger fehlerfrei angekommen ist.

___

## Bestätigungsformen

### ACK
-> acknowledgement, positiv.

### NAK
-> negative acknowledgement, negativ. Wird verwendet, um Retransmission noch vor Ablauf der RTO zu veranlassen.

___

## Drei ARQ-Verfahren:

### Stop-and-Wait

-> Auch: **Send-and-Wait**.

Das **einfachste** zu implementierende Verfahren, allerdings nicht effizient. Die maximal nutzbare Bandbreite hängt von der **Round-Trip-Time** ab, es kann also nur ein **Bruchteil der verfügbaren Bandbreite** genutzt werden.

Dabei wird nach dem Versenden eines **jeden** Datenpakets auf die Bestätigung des Empfängers gewartet, bevor das nächste Paket auf den Weg geschickt wird. 

Falls Bestätigung ausbleibt -> **Retransmission**. Es darf also maximal **ein** unbestätigtes Paket existieren!


### Go-back-N

Effizienter als Stop-and-Wait. Die Anzahl der unbestätigten Pakete hängt von der **Fenstergröße N** ab. Es dürfen maximal **N** unbestätigte Pakete existieren.

Kommt es zum **Timeout**, werden alle Datenpakete der Fensters retransmittet. Alle nachfolgenden Pakete werden **verworfen**.


### Selective-Repeat

-> Weiterentwicklung von **Go-back-N**. Wird ein Paket nicht empfangen, so werden alle nachfolgenden Pakete nicht verworfen, sondern in einen **Empfangbuffer** zwischengespeichert und korrekt bestätigt.

Bei einem Timeout werden **nuir nicht bestätigte Pakete** neu gesendet, anstelle aller Pakete des Fensters.
