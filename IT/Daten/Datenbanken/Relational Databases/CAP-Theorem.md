# CAP-Theorem

Nur **2 der 3** folgenden Punkte auf einem System implementierbar:

* **Consistency**
  -> Nach einer Transaktion sollen die Daten für *alle* Parteien verändert werden.
* **Availability** -> Das System muss in angemessener Zeit auf jegliche Anfrage antworten
* **Partition Tolerance** -> Auch wenn einzelne Nodes außer Gefecht sind, funktioniert das System noch.


![[zDrawing_CAP]]


**CP** -> Daten könnten nicht erreichbar sein
**PA** -> Client könnte inkonsistente Daten lesen
**CA** -> Netzwerkprobleme könnten System lahmlegen ^67233d