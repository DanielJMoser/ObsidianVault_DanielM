#Datenbanken #Datennetze 

-> ein Algorithmus zur [[Traversierung]] von Graphen. 

Der Algorithmus besucht alle Knoten eines Graphen, indem er sich auf einen **Startknoten** festlegt und dann **rekursiv den nächsten unbesuchten Knoten besucht**, bis alle Knoten besucht wurden. Dabei geht er möglichst tief in die Tiefe eines Astes, bevor er zu einem anderen Ast wechselt.

Hier ist ein Beispiel zur Verdeutlichung:

Angenommen, wir haben einen Graphen mit den Knoten _A, B, C, D, E_ und _F_ und den Kanten *(A,B), (A,C), (B,D), (C,E)* und *(E,F)*. Wenn wir den Depth-First Search Algorithmus auf diesen Graphen anwenden und den Startknoten *A* wählen, würde der Algorithmus wie folgt vorgehen:

1.  Besuche Knoten A
2.  Besuche Knoten B
3.  Besuche Knoten D
4.  Keine weiteren unbesuchten Knoten in D's Ast, kehre zum Knoten B zurück
5.  Besuche Knoten C
6.  Besuche Knoten E
7.  Besuche Knoten F
8.  Keine weiteren unbesuchten Knoten in F's Ast, kehre zum Knoten E zurück
9.  Keine weiteren unbesuchten Knoten in E's Ast, kehre zum Knoten C zurück
10.  Keine weiteren unbesuchten Knoten in C's Ast, kehre zum Knoten A zurück
11.  Keine weiteren unbesuchten Knoten in A's Ast, der Algorithmus ist beendet

Durch die Rekursion geht DFS möglichst tief in die Tiefe eines Astes, bevor es zu einem anderen Ast wechselt. Dadurch eignet sich der Algorithmus besonders gut für Aufgaben wie das Finden von Pfaden in einem Graphen oder das Erkennen von Zyklen in einem Graphen. Auch in der Künstlichen Intelligenz wird DFS oft verwendet, z.B. in der Suche nach Lösungen in einem Spiel wie Schach.****