**Nodes** sind ein wesentlicher Bestandteil von **Graphen**, die in **[[IT/Daten/Datenbanken/NoSQL Databases/Neo4j/Neo4j]]** Datenbanken verwendet werden. Ein Knoten ist ein Objekt, das Daten repräsentiert, das in Beziehung zu anderen Objekten in der Datenbank steht. In der Regel sind Knoten durch **Kanten** miteinander verbunden, um Beziehungen zu definieren.

## Eigenschaften

Ein Knoten besteht aus einem eindeutigen Identifikator, der als **ID** bezeichnet wird, und einem Satz von Attributen, die als **Eigenschaften** bezeichnet werden. Jede Eigenschaft hat einen Namen und einen zugehörigen Wert.

Die Eigenschaften können in jeder beliebigen Anzahl und Kombination vorhanden sein, um spezifische Informationen für einen Knoten zu speichern. Sie können beispielsweise die Attribute eines Benutzers in einer sozialen Netzwerk-App oder eines Produkts in einem E-Commerce-System darstellen.

## Labels

Um die verschiedenen Arten von Knoten in einer Datenbank zu unterscheiden, können **Labels** verwendet werden. Ein Label ist eine Kennzeichnung, die einem Knoten zugeordnet wird, um eine Kategorie oder einen Typ darzustellen. Ein Knoten kann mehrere Labels haben, um seine verschiedenen Eigenschaften oder Rollen in der Datenbank zu repräsentieren.

Ein Beispiel dafür ist ein soziales Netzwerk, bei dem Benutzer, Beiträge, Kommentare und Gruppen verschiedene Labels haben können. Dadurch können Abfragen einfach auf spezifische Knotentypen eingeschränkt werden, ohne alle Knoten in der Datenbank durchsuchen zu müssen.

## Abfrage von Knoten

Um Knoten in Neo4j abzufragen, wird die **Cypher-Abfragesprache** verwendet. Mit Cypher können Knoten und Kanten auf verschiedene Weise abgefragt werden, um Beziehungen zwischen den Objekten in der Datenbank zu definieren.

Eine einfache Abfrage, um alle Knoten in der Datenbank abzurufen, lautet wie folgt:

```sql
`MATCH (n) MATCH (n) RETURN n`
```

Dies gibt eine Liste aller Knoten in der Datenbank zurück.


### Syntax

In der [[Cypher]]-Abfragesprache wird ein Knoten in geschweiften Klammern dargestellt:

```cypher
({label: value, label: value})
```

Dabei steht `label` für den Namen der Eigenschaft und `value` für den Wert. 
Ein Knoten kann mehrere Label und Eigenschaften haben, wobei jedes Label durch einen Doppelpunkt getrennt ist und jede Eigenschaft durch ein Komma getrennt ist.

### Beispiel

Angenommen, wir möchten einen Graphen erstellen, der Personen und ihre Beziehungen zu anderen Personen darstellt. Wir können jeden Menschen als Knoten darstellen, wobei jeder Knoten eine `name`-Eigenschaft und ein `age`-Label hat:

```cypher
({name: 'Alice', age: 30})

({name: 'Bob', age: 35})

```

Wir können auch Beziehungen zwischen Personen durch Kanten darstellen. Angenommen, Alice und Bob sind Freunde. Wir können dies durch eine Kante darstellen, die die beiden Knoten verbindet:

```cypher
({name: 'Alice', age: 30})-[:FRIENDS_WITH]->({name: 'Bob', age: 35})
```


In diesem Beispiel haben wir eine Kante mit dem Typ `FRIENDS_WITH` erstellt, die Alice und Bob verbindet.