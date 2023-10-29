#Datennetze 

-> Nachrichten werden in einzelne **Datenpakete** aufgeteilt, die dann über **gemeinsam genutzte Verbindungen** an den Empfänger geschickt werden.

Die Pakete durchqueren das Netz dabei als **unabhängige** und **eigenständige** Einheiten. Das Netz kann ein Paket _keinem Kommunikationsvorgang zuordnen,_ weshalb Zwischenknoten auch **keine** Verbindungszustandsinformationen speichern müssen.

Auch können Pakete mit dem selben Verbindungsziel **unterschiedliche Routen** nehmen und in **anderer Reihenfolge** als urspr. verschickt ankommen.

Ein **expliziter** Verbindungsaufbau am Anfang ist **nicht** notwendig! Ein bekanntes Beispiel ist das **klassische Postsystem.**

___

### Vorteile:

- **Effiziente** Bandbreitennutzung.
- Ausfall eines Knoten bzw. einer Zwischenverbindung führt **nicht zum Abbruch** der Kommunikation.
- **Keine Verbindungszustandsinformation** in den Zwischenknoten notwendig.
  - Dadurch: **Unbegrenzte** Anzahl an Verbindungen möglich.
- **Kein Verbindungsaufbau** notwendig.


### Nachteile:

- Keine Bandbreitenzusicherung.
- Schwankende und generell höhere [[Eigenschaften einer Datenverbindung#Latenz|Latenzen]].
- Daten kommen u.U. **nicht in der richtigen Reihenfolge** an.

Gemeinsam genutzte Verbindungen bedeuten auch, dass es zu **Engpässen** und **Staus** kommen kann. Besonders gefährdet sind Übergänge von Netzteilen mit hoher Bandbreite zu Netzteilen mit niedriger Bandbreite.

Treten solche Engpässe auf, werden in den Netzknoten Pakete in sog. **Queues** zwischengespeichertm was wiederrum die [[Eigenschaften einer Datenverbindung#Latenz|Latenz]] steigert 
-> genannt **Queueing Delay**!
Ist diese warteschlange voll, so gehen neuankommende Pakete verloren!

___

Solche Systeme funktionieren nach dem **Best-Effort-Prinzip**. Durch **zusätzliche Maßnahmen** können manche Eigenschaften (z.B. Fehlerfreiheit oder Vollständigkeit) dennoch garantiert werden. Ein Beispiel dafür ist [[TCP]].


