**Relationships** sind in der Datenmodellierung die Verbindungen zwischen den **Knoten** einer Datenbank. In **Cypher** können Beziehungen zwischen Knoten mithilfe des Schlüsselwortes `MATCH` gefunden werden.

### Erstellen von Relationships

In Cypher können Beziehungen zwischen Knoten auf verschiedene Arten erstellt werden. Die einfachste Möglichkeit ist die Verwendung des Schlüsselwortes `CREATE`. Zum Beispiel, um eine Beziehung zwischen einem `Person`-Knoten und einem `Place`-Knoten mit dem Attribut `name` zu erstellen, können Sie den folgenden Code ausführen:

```cypher
CREATE (:Person)-[:VISITED {name {name: 'New York City'}]->(:Place)
```

## Relationships bei Cypher

**Relationships** sind in der Datenmodellierung die Verbindungen zwischen den **Knoten** einer Datenbank. In **Cypher** können Beziehungen zwischen Knoten mithilfe des Schlüsselwortes `MATCH` gefunden werden.

### Erstellen von Relationships

In Cypher können Beziehungen zwischen Knoten auf verschiedene Arten erstellt werden. Die einfachste Möglichkeit ist die Verwendung des Schlüsselwortes `CREATE`. Zum Beispiel, um eine Beziehung zwischen einem `Person`-Knoten und einem `Place`-Knoten mit dem Attribut `name` zu erstellen, können Sie den folgenden Code ausführen:


```cypher
CREATE (:Person)-[:VISITED {name  {name: 'New York City'}]->(:Place)
```


Hier wird eine Beziehung mit dem Typ `VISITED` erstellt, die von einem `Person`-Knoten zu einem `Place`-Knoten führt, wobei das Attribut `name` als Eigenschaft der Beziehung festgelegt wird.

### Abfragen von Relationships

Beziehungen können mithilfe des `MATCH`-Schlüsselworts abgefragt werden. Beispielsweise können Sie alle `Person`-Knoten abrufen, die `New York City` besucht haben, indem Sie den folgenden Code ausführen:

```cypher
MATCH (:Person)-[v:VISITED]->(:Place {name: }) RETURN v MATCH (:Person)-[v:VISITED]->(:Place {name: 'New York City'}) RETURN v
```

### Löschen von Relationships

In Cypher können Beziehungen mit dem Schlüsselwort `DELETE` gelöscht werden. Beispielsweise können Sie alle Beziehungen mit dem Typ `VISITED` löschen, indem Sie den folgenden Code ausführen:

```cypher
MATCH (:Person)-->(:Place) DELETE v MATCH (:Person)-[v:VISITED]->(:Place) DELETE v
```

Hier wird die Beziehung mit dem Typ `VISITED` abgefragt und dann mit dem `DELETE`-Schlüsselwort gelöscht.

### Filtern von Relationships

Beziehungen können auch mithilfe von Filtern abgefragt werden. Beispielsweise können Sie alle `Person`-Knoten abrufen, die `New York City` besucht haben und die in den Jahren zwischen 2010 und 2015 geboren wurden, indem Sie den folgenden Code ausführen:

```cypher
MATCH (:Person)-[v:VISITED MATCH (p:Person)-[v:VISITED]->(:Place {name: 'New York City'}) WHERE p.birth_year >= 2010 AND p.birth_year <= 2015 RETURN p
```
Hier werden die `Person`-Knoten abgefragt, die eine Beziehung mit dem Typ `VISITED` zu einem `Place`-Knoten mit dem Attribut `name` `New York City `New York City` haben und deren `birth_year`-Attribut innerhalb des gewünschten Bereichs liegt.