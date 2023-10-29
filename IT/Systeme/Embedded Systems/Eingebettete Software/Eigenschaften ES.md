# Eigenschaften
#embeddedsystems

-> Drei Kerneigenschaften:

* **niedriger Energieverbrauch
* **Verlässlichkeit
* **Echtzeitfähigkeit


## Energieverbrauch

Dieser soll möglichst niedrig sein, bei Batteriebetriebenen Systemen oft im Milliwattbereich. 

"Verbrauchte" Energie wird als **Wärme** wieder abgeführt.
Hitzeableitsysteme sind bei [[_Mikrocontroller#System-on-a-Chip|SoC]]s oft schwierig oder unmöglich zu realisieren. Daher oft **höhere Betriebstemperaturen** als bei anderen Computersystemen.

----------------------------------------------

## Verlässlichkeit

#### Zuverlässigkeit

* Wahrscheinlichkeit, dass eine vorgegebene Funktion über einem bestimmten Zeitraum fehlerfrei ausgeführt wird.
* Der resultierende Erwartungswert wird **"Mean Time Between Failures"** (MTBF) genannt.
* Eingebettete Systeme bestehen hierbei auf höhere Standards als andere Computersysteme.


#### Verfügbarkeit

* Anteil der **fehlerfreien Laufzeit** eines Systems.
$$Verfügbarkeit = \frac{Gesamtzeit - Ausfallzeit} {Gesamtzeit}$$

#### Funktionale Sicherheit

* Nicht akzeptierbare Risiken (etwa die Gefährdung von Menschenleben) müssen **weitgehend ausgeschlossen* werden!
* Andere Risiken (etwa Verletzungsrisiken) **auf ein akzeptierbares Maß reduziert** werden.
$$Risikomaß = Eintrittswahrscheinlichkeit * Kosten$$

## [[Echtzeitsysteme|Echtzeitfähigkeit bei Embedded Systems]]

-> der Betrieb eines Rechnersystems, bei dem Programme zur Verarbeitung anfallender Daten **selbstständig bereit** sind, derart, dass die Verarbeitungsergebnisse **innerhalb einer vorgegebenen Zeitspanne verfügbar** sind.

Oftmals strikte Vorgaben bei [[_Embedded Systems|Embedded Systems]], da Sicherheitsrisiken entstehen könnten.