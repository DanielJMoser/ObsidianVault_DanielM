
## Persistence Layer generell

Ein **Persistence Layer** ist eine Schicht in einer Anwendung, die für die **Speicherung** und den **Zugriff** auf Datenbanken oder andere persistente Datenspeicher verantwortlich ist. 

Der Persistence Layer **versteckt** die Details der Datenbankinteraktion vor dem Rest der Anwendung und ermöglicht es Entwicklern, sich auf die **Geschäftslogik** zu konzentrieren, anstatt sich mit den Details der Datenbankinteraktion auseinandersetzen zu müssen.

Ein Persistence Layer besteht normalerweise aus einer **Reihe von Klassen** und **Methoden**, die für die 
- Verwaltung von Datenbankverbindungen, 
- die Erstellung und Ausführung von SQL-Abfragen, 
- die Zuordnung von Datenbankdaten zu Objekten und 
- die Verwaltung von Transaktionen verantwortlich sind. 

Oft werden Frameworks wie **Hibernate**, **JPA** (Java Persistence API) oder **Spring** verwendet, um die Entwicklung des Persistence Layers zu vereinfachen und zu beschleunigen.

___

## Anwendungsbeispiel

Ein typisches Beispiel für die Verwendung eines Persistence Layers ist eine **Webanwendung, die Daten aus einer Datenbank liest und schreibt.** 

Der Persistence Layer der Anwendung ist für das **Speichern der Daten** in der Datenbank und für das **Abrufen der Daten** aus der Datenbank verantwortlich.
Der Rest der Anwendung kann sich auf die Verarbeitung der Daten konzentrieren, ohne sich um die Details der Datenbankinteraktion kümmern zu müssen.

___

