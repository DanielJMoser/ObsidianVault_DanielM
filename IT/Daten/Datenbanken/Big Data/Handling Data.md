#BigData
Unternehmen sammeln eine Fülle von Daten, die nützliche Erkenntnisse und Erkenntnisse liefern können, um ihre Geschäftsprozesse zu optimieren. 
Allerdings muss man diese Daten auch entsprechend **verwalten** und **speichern**, um sie effektiv nutzen zu können. I

m Folgenden werden drei gängige Ansätze zur Verwaltung von Daten beschrieben: **Data Lake**, **Data Warehouse** und **Data Mart**.

### Data Lake

Ein **Data Lake** ist eine [[_Datenstrukturen|Datenstruktur]], die es Unternehmen ermöglicht, große Mengen an Rohdaten zu speichern. 
Im Gegensatz zu einem Data Warehouse ist ein Data Lake darauf ausgelegt, **alle** Arten von Daten zu speichern, egal ob sie [[Variety#1. Strukturierte Daten|strukturiert]], [[Variety#3. Unstrukturierte Daten|unstrukturiert]] oder [[Variety#2. Semi-strukturierte Daten|semi-strukturiert]] sind. 
In einem Data Lake werden Daten in der Regel **ohne vorherige Modellierung oder Aggregation** gespeichert.

#### Vorteile

-   _Skalierbarkeit_: Ein Data Lake kann problemlos skaliert werden, um mit dem Wachstum der Datenmenge Schritt zu halten.
-   _Flexibilität_: Alle Arten von Daten können im Data Lake gespeichert werden, unabhängig von ihrer Struktur oder Herkunft.
-   _Geringe Kosten_: Da keine Modellierung oder Aggregation erforderlich ist, sind die Kosten für die Speicherung von Daten in einem Data Lake im Allgemeinen niedriger als bei anderen Ansätzen.

#### Nachteile

-   _Komplexität_: Aufgrund der Vielzahl von Daten, die im Data Lake gespeichert werden, kann es schwierig sein, spezifische Daten zu finden oder zu identifizieren.
-   _Datenqualität_: Ohne Modellierung oder Aggregation kann es schwierig sein, Daten zu validieren oder zu überprüfen, was zu einer geringeren Datenqualität führen kann.

___

### Data Warehouse

Ein **Data Warehouse** ist eine zentrale Datenbank, die Unternehmen zur Speicherung, Verwaltung und Analyse von Daten verwenden. I
m Gegensatz zu einem Data Lake werden in einem Data Warehouse Daten **strukturiert, modelliert und aggregiert**, um Berichte, Analysen und Prognosen zu erstellen.

#### Vorteile

-   _Hohe Datenqualität_: Durch Modellierung und Aggregation werden Daten bereinigt und validiert, was zu einer höheren Datenqualität führt.
-   _Einfache Abfrage_: Da Daten im Data Warehouse strukturiert sind, können sie einfacher abgefragt werden als im Data Lake.
-   _Schnelle Leistung_: Ein Data Warehouse ist darauf ausgelegt, Abfragen schnell auszuführen, was die Leistung und Geschwindigkeit von Analysen und Berichten verbessert.

#### Nachteile

-   _Hohe Kosten_: Die Modellierung und Aggregation von Daten erfordert zusätzliche Arbeit und Ressourcen, was zu höheren Kosten führt.
-   _Mangel an Flexibilität_: Ein Data Warehouse ist auf eine bestimmte Struktur und Anwendung ausgelegt, was die Verwendung von Daten für andere Zwecke erschweren kann.

___


### Data Mart

Ein **Data Mart** ist eine spezialisierte Datenbank, die spezifische Daten für bestimmte Abteilungen oder Zwecke bereitstellt. 
Im Gegensatz zu einem Data Warehouse, das alle Daten enthält, werden in einem Data Mart nur die Daten gespeichert, die für eine **bestimmte Anwendung oder Analyse relevant** sind.

#### Vorteile

-   _Schnellere Abfrageleistung_: Da Data Marts nur einen Teil der Daten enthalten, die für eine spezifische Gruppe von Benutzern relevant sind, können Abfragen schneller ausgeführt werden als bei einer vollständigen Data Warehouse-Abfrage.
-   _Bessere Datenqualität_: Data Marts können auf spezifische Geschäftsbereiche ausgerichtet sein, was zu einer besseren Datenqualität führt, da sie auf die Bedürfnisse dieser Geschäftsbereiche zugeschnitten sind.
-   _Benutzerfreundlichkeit_: Data Marts sind in der Regel benutzerfreundlicher als Data Warehouses, da sie spezifische Daten enthalten, die auf die Bedürfnisse der Benutzer zugeschnitten sind.

#### Nachteile

-   _Datenredundanz_: Data Marts können zu einer Redundanz von Daten führen, da bestimmte Daten in mehreren Marts dupliziert werden können.
-   _Eingeschränkte Datenverfügbarkeit_: Da Data Marts nur einen Teil der Daten enthalten, die im Data Warehouse gespeichert sind, können Benutzer auf wichtige Daten zugreifen, die möglicherweise in anderen Marts nicht verfügbar sind.
-   _Hohe Kosten_: Der Aufbau von Data Marts kann teuer sein, insbesondere wenn mehrere Marts erforderlich sind, um die Bedürfnisse aller Geschäftsbereiche zu erfüllen.