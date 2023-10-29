-> Verfahren zum Durchsuchen eines Graphen oder Baums. 
Es beginnt an der **Wurzel** und erkundet alle benachbarten Knoten auf der gleichen Ebene, bevor es in die nächste Ebene absteigt. Es nutzt eine Warteschlange, um die Reihenfolge der zu besuchenden Knoten zu verwalten.

BFS eignet sich besonders für die Suche nach kürzesten Pfaden in ungewichteten Graphen. Es hat eine Zeitkomplexität von **O(|V| + |E|)**, wobei |V| die Anzahl der Knoten und |E| die Anzahl der Kanten im Graphen sind.

Ein Algorithmus für BFS sieht folgendermaßen aus:

1.  Füge den Startknoten in eine Warteschlange ein.
2.  Während die Warteschlange nicht leer ist:
    1.  Entnimm den ersten Knoten aus der Warteschlange.
    2.  Wenn der Knoten das Ziel ist, gib den Pfad aus und beende den Algorithmus.
    3.  Füge alle unbesuchten Nachbarn des Knotens in die Warteschlange ein und markiere sie als besucht.

BFS ist auch eine grundlegende Komponente vieler Algorithmus-Design-Methoden, wie zum Beispiel dem [[Dijkstra]]-Algorithmus für kürzeste Pfade in gewichteten Graphen und dem A*-Algorithmus für Heuristik-Suche.