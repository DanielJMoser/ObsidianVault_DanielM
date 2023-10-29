#Datennetze 

-> [[IP]]

Eine solche Adresse ist **32-bit** groß, es gibt also etwa **4,3 Milliarden** Stück davon.

___

## Aufbau

Bestehend aus **Netzanteil** und **Hostanteil**.

- **Netzanteil**: steht vor dem Hostteil und identifiziert das Teilnetz.
- **Hostanteil**: identifiziert ein Gerät innerhalb des Teilnetzes.

Die Größe von beidigem ist variabel.

___

## Notation

Jedes der **vier Byte** der Adresse wird als **Dezimalzahl** geschrieben. Dabei werden die einzelnen Bytes durch **Punkte** getrennt.

**192.168.20.43**


Die Größe des Netzanteils wird durch die **Subnetzmaske** angegeben.
Dabei handelt es sich (ebenfalls) um eine 32-bit-Zahl. Die **"1er-Stellen"** sind dabei jene, die zur IP-Adresse gehören. Notation gleich wie IP!

**255.255.255.0** -> 24-bit Netzanteil, 8-bit Hostanteil.


**Beispiel:**

IP:                         <mark style="background: #FFB86CA6;">10.2</mark>.<mark style="background: #D2B3FFA6;">1.3</mark>
Subnetzmaske:   <mark style="background: #FFB86CA6;">255.255</mark>.<mark style="background: #D2B3FFA6;">0.0</mark>

<mark style="background: #FFB86CA6;">Netzanteil</mark>, <mark style="background: #D2B3FFA6;">Hostanteil</mark>


___

## Spezielle Adressbereiche

Manche Adressblöcke sind für **spezielle Zwecke** reserviert. Eine Auswahl:

- Adressbereiche für **private Netzwerke** (werden nicht im Internet geroutet)
  - 10.0.0.0/8
  - 192.168.0.0/16
 
- **Loopback-Adressbereich**: 127.0.0.0/8
  - nur lokal am selben Rechner erreichbar
  - z.B. **localhost**-Adresse: 127.0.0.1
  - Kann auch für **Inter-Process-Communication** verwendet werden (interessant für Anwendungsentwicklung, da kein externer Server benötigt).