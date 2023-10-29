# Abtastung
#embeddedsystems

## Abtastfrequenzen

#### Nyquist-Shannon-Theorem
> Ein auf **f(max)** banbegrenztes Signal kann aus deiner Folge äquedistanten Abtastwerten **exakt** rekonstruiert werden, wenn die Abtrastfrequenz größer als **2 * f(max)** ist.

-> "auf f(max) begenzt": Kein Wert größer als f(max).

Da in der Praxis noch **Messfehler** und **Rauschen** hinzukommen, kann ein Signal nicht wirklich exakt rekonstruiert werden. 
***Je größer allerdings die Abtastfrequenz, desto genauer die Rekonstruktion!***


#### Alias-Effekt

-> auch: *Aliasing-Effekt, Aliasing*

Enthält das abzutastende Signal Frequenzanteile, die **höher als die halbe Abtastfrequenz** sind, kommen im rekonstruierten Signal **im Originalsignal nicht vorhandene Frequenzen** vor.

Häufige Fehlerquelle: **Rauschen**! Um diese zu umgehen, werden Signale ***vor*** ihrer Digitalisierung durch einen Tiefpass (*Anti-Aliasing-Filter*) gefiltert.

