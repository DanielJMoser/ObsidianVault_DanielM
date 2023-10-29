**Cypher** ist eine deklarative Abfragesprache, die speziell für 
[[IT/Daten/Datenbanken/NoSQL Databases/Neo4j/Neo4j]] entwickelt wurde, eine **Graphdatenbank**. Die Sprache wurde erstmals im Jahr 2012 veröffentlicht und ist jetzt eine der wichtigsten Methoden zur Abfrage von Graphdatenbanken.

### Funktionen

Cypher ermöglicht es Benutzern, **Daten zu abstrahieren**, um sie als Graphen darzustellen und zu verwalten. Eine Abfrage in Cypher beginnt immer mit dem Keyword "MATCH", gefolgt von der Beschreibung des Graphen, auf dem die Abfrage ausgeführt wird.

### Beispiele

Ein Beispiel für eine einfache Cypher-Abfrage wäre:

```less
MATCH (n:Person)-[:FOLLOWS]->(m:Person)
RETURN n.name, m.name
```

Dies würde eine Abfrage auf einer Graphdatenbank ausführen, die Personen als Knoten und "**FOLLOWS**"-Beziehungen zwischen diesen Knoten aufweist. Die Abfrage würde dann die Namen aller Personen zurückgeben, die über eine solche Beziehung miteinander verbunden sind.

### Eigenschaften

Cypher ist eine **deklarative Sprache**, was bedeutet, dass Benutzer die Ergebnisse beschreiben, die sie erhalten möchten, anstatt spezifische Schritte zu beschreiben, die zum Erreichen dieser Ergebnisse unternommen werden müssen. Dies macht es für Benutzer einfacher, Abfragen zu erstellen, da sie sich auf das **"Was** konzentrieren können, anstatt auf das "**Wie**".

Cypher unterstützt auch **Pattern-Matching**-Syntax, die es Benutzern ermöglicht, Abfragen durchzuführen, indem sie Beziehungen zwischen Knoten innerhalb eines Graphen suchen. Es unterstützt auch **Aggregation**-Funktionen, die es Benutzern ermöglichen, Gruppen von Knoten oder Beziehungen zu aggregieren und zu analysieren.

### Anwendungen

Cypher wird hauptsächlich in Verbindung mit Graphdatenbanken wie [[IT/Daten/Datenbanken/NoSQL Databases/Neo4j/Neo4j]] verwendet, ist aber auch mit anderen Datenbanken wie SAP HANA und AgensGraph kompatibel. Es wird in verschiedenen Anwendungen eingesetzt, darunter Netzwerk- und IT-Sicherheit, Betrugserkennung, Sozialnetzwerkanalyse und Wissensmanagement.