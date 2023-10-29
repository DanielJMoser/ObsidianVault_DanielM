-> Graphdatenbank, die sich auf die Verwaltung von Daten in Form von **Knoten** und **Kanten** konzentriert. Im Gegensatz zu traditionellen relationalen Datenbanken, die auf Tabellen basieren, speichert Neo4j Daten in Form eines Graphen. Dies ermöglicht es Benutzern, komplexe Beziehungen zwischen Datenpunkten auf eine einfache und effektive Weise zu modellieren und abzufragen.

## Datenmodell

Neo4j verwendet ein datenorientiertes Datenmodell, das aus **Knoten**, **Kanten** und **Eigenschaften** besteht. 
Knoten repräsentieren [[Entity|Entitäten]], während Kanten **Beziehungen** zwischen ihnen darstellen. Eigenschaften sind **Schlüssel-Wert-Paare**, die an Knoten oder Kanten angehängt werden können, um zusätzliche Informationen zu speichern.

### Graph-Datenmodellierung

Das Graph-Datenmodell ermöglicht es, Datenstrukturen als Knoten und Kanten zu modellieren. Jeder Knoten und jede Kante kann beliebig viele Eigenschaften enthalten, die entweder primitiv oder komplexe Datentypen sein können. Die Daten werden in einer hierarchischen Struktur organisiert und ermöglichen eine schnelle Navigation durch komplexe Beziehungen.

___

## Query Language

Neo4j verwendet die **Cypher-Abfragesprache**, um Datenabfragen durchzuführen. Cypher ähnelt der SQL-Sprache, die für relationale Datenbanken verwendet wird, aber mit einigen wichtigen Unterschieden. Cypher ermöglicht es Benutzern, Daten als Graphen zu modellieren und Abfragen mit einer einfachen Syntax auszuführen. Eine Cypher-Abfrage beginnt typischerweise mit der Angabe des Musters, das zurückgegeben werden soll, gefolgt von optionalen Bedingungen und Filtern.

___

## Besonderheiten

### Skalierbarkeit

Neo4j ist sehr skalierbar und unterstützt verteilte Datenverarbeitung über mehrere Server. Es verwendet einen Ansatz namens "Sharding", um große Datenmengen zu verarbeiten, indem es den Datenbestand horizontal partitioniert und auf mehrere Knoten verteilt.

### ACID-Transaktionen

Neo4j garantiert die Einhaltung der [[ACID]]-Eigenschaften (Atomicity, Consistency, Isolation, Durability) für alle Transaktionen, um Datenkonsistenz und Integrität zu gewährleisten.

### Performance

Neo4j ist auf die Verarbeitung von Graphdaten spezialisiert und bietet daher eine höhere Leistung bei der Verarbeitung von Abfragen, die Beziehungen zwischen Datenpunkten beinhalten. Die Speicherung von Daten im Arbeitsspeicher und die Nutzung von Indexen tragen ebenfalls zu einer schnelleren Abfrageverarbeitung bei.

### Flexibilität

Durch die Verwendung des Graph-Datenmodells ist Neo4j sehr flexibel und ermöglicht eine einfache Änderung von Datenmodellen, ohne dass komplexe Migrationen erforderlich sind.

### Anwendungen

Neo4j wird in verschiedenen Anwendungsbereichen eingesetzt, darunter:

-   **Social Networking**Social Networking**: Empfehlungssysteme, Freundesempfehlungen und Community-Detection
-   **Fraud Detection**Fraud Detection**: Erkennung von Betrugsmustern in Finanztransaktionen