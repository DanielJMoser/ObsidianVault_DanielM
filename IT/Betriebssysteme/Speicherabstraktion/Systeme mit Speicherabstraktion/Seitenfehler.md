
Weiste eine [[Adressraum|Adresse]] auf einen Eintrag mit **Present-Bit 0**, so komme es zu einem **Page Fault** (zu deutsch: Seitenfehler).
Hier übernimmt das Betriebssystem und löst eben diesen Seitenfehler auf.

## Auflösen

siehe auch: [[Paging]]
- Ist der Rahmen noch nicht eingehängt, so wird ein **freier** gesucht und, naja, eingehängt. 
- Wurde der Rahmen **ausgelagert**, so wird er von der **Auslagerungsdatei** geholt und eingehängt.
- Ist die Seite tatsächlich ungültig, wird ein **Segmentation Fault** ausgelöst.
  Der "Segmentation Fault" moderner Betriebssysteme ist demnach kein eigentlicher Fehler der [[Segmentierung]], sondern vielmehr ein **Überbleibsel** aus Zeiten der Systeme **ohne Speicherabstraktion**.
  

___


## Seitentabellen

-> Bildet den **gesamten virtuellen Adressraum** ab.

Einstufige Seitentabellen werden i.d.R. **vollständig** im Speicher abgelegt. Solche Tabellen sind bei **großem Arbeitsspeicher ineffizient!**

Effizientere Arten der Organisation sind
- mehrstuftige Seitentabellen
- invertierte Seitentabellen


### Mehrstufige Seitentabelle

Eine Adresse führt zur **ersten Stufe** einer Tabelle. Jeder derer Slots (jede der virtuellen Seiten) führt zu Tabellen **zweiter Stufe**, usw.
Dieses Auslagerungsverfahren bietet besondere **flexibilität**.

![[zzDrawing_mehrstufigeSeitentabelle.png]]




## Seitenauslagerung

![[zzDrawing_Seitenauslagerung.png]]