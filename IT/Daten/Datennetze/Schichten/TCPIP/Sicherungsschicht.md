#Datennetze 

Schickt Datenpakete mittels [[Router]] entlang dem von der [[4. Schicht -> Transportschicht]] gefundenen Weg weiter.

___

## Maximum Transition Unit (MTU)

-> gibt die maximale Größe eines IP-Pakets an, die über eine Verbindung transportiert werden kann. Diese hängt von der **Technologie der Sicherungsschicht** ab.

z.B:

- **Ethernet**: 1500 Byte
- **Wlan**: 2312 Byte
- **ATM**: 4500 Byte
- **Jumboframes** (d.i. Gigabit-Ethernet): 9000 Bytes


## Fragmentierung

Unter Umständen ist ein Paket zu groß für die jeweilige Verbindung, was durch **Fragmentierung** gelöst wird.
Dabei wird es in mehrere Teile zerlegt, welche als einzelne Pakete versendet und vom Empfänger wieder zusammengebaut werden.

Da Fragmentierung zu **Leistungseinbußen** und erhöhter **Verlustwahrscheinlichkeit** führt, sollte es möglichst vermieden und kann auch (via der "Don't Fragment"-Flag, DF-Flag) ausgeschalten werden. Zu größe Pakete werden bei gesetzter Flag **verworfen**, der Sender benachrichtigt.

### Korrektes Zusammensetzen

siehe: [[IP-Header]]

Das **Identification**-Feld kennzeichnet zusammengehörige Fragmente.
Das **Fragment Offset**-Feld gibt die Position der einzelnen Fragmenten an.
Die **MF**-Flag (d.i. More Fragments) erlaubt die Erkennung des letzten Fragments.

