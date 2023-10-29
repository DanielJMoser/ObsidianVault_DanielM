#Datenstrukturen 

Angenommen, wir wollten ein Set von Strings in eine Hashtabelle speichern:

{“ab”, “cd”, “efg”}

Das Hauptaugenmerk liegt dabei darin, Werte zu **suchen** und **speichern**, nicht die Reihenfolge der eingeordneten Strings.

1) Wir wissen, dass [[Hashfunktion|Hashfunktionen]] dazu dienen, den **Hashwert** zu berechnen, welcher den **Index** innerhalb der [[_Datenstrukturen|Datenstruktur]] beschreibt, unter welchem der Wert gespeichert wird.
2) "a" = 1; "b" = 2; usw.
3)  Dadurch ergibt sich durch Summierung der numerischen Werte der Strings:
   $$\mathcal{'ab'} = 1 + 2 = 3$$
    $$\mathcal{'cd'} = 3 + 4 = 7$$
     $$\mathcal{'efg'} = 5 + 6 + 7 = 18$$

4) 
