# Adressraum

-> ***Menge eindeutiger Adressen, die ein Prozess zur adressierung verwenden kann***.

Seine maximale Größe wird durch die **Größe der Speicheradressen** bestimmt.

_____

## Arten von Adressräumen


### Flacher/Linearer Adressraum

* Besteht aus **monoton ansteigenden** Adressen **ohne Hierarchie**
* z.B. 0 - 65535 bei 16-Bit Adressen.


### Segmentierter Adressraum

* Adressraum in Segmente unterteilt, die wiederrum eigene Adressräume bilden.
* z.B. entspricht Adresse "4" im Segment "1" einer andrern Speicherzeile als Adresse "4" im Segment "3".


### Hierarchischer Adressraum

* Hierarchischer Aufbau
* z.B. Postanschrift: Land -> Stadt -> Straße -> Hausnummer

___

## Physischer Adressraum

* Menge an **physisch ansprechbaren** Adressen
* Verbauter Speicher + Memory-Mapped I/O + sonstige reservierte Bereiche
* Nutzt i.d.R. nicht maximal verfügbaren Adressraum.
* Kann Lücken aufweisen!
* i.d.R. ein [[Adressraum#Flacher Linearer Adressraum|Flacher, Linearer Adressraum]]


## Virtueller Speicher

* Jedem Prozess ein vom [[Adressraum#Physischer Adressraum|Physischen Adressraum]] unabhängiger  Adressraum. So kann dieser **komplett** audgenutzt werden (löst also das [[Relokationsproblem]])!
* Speicher adressiert so mehr Bereiche, als physisch vorhanden.
* Virtuelle Speicherbereiche werden auf andere Speicherräume abgebildet (i.d.R **Physische Speicherbereiche**, aber auch **Sekundärspeicher**)

Siehe: [[Paging]]
