
| Name       | Address      | Email          |
| ---------- | ------------ | -------------- |
| John Smith | 123 Main Str | john@smith.com |
| Jane Doe   | 456 Park Ave | jane@doe.com   |


In einer [[_Relationale Datenbanken|relationalen Datenbank]] ist ein Fremdschlüssel ein **Feld oder ein Satz von Feldern**, der dazu dient, eine V**erbindung zwischen den Daten** in zwei Tabellen herzustellen.
Er wird verwendet, um die _referentielle Integrität_ zu erzwingen, die sicherstellt, dass die Daten in den Bezugstabellen **konsistent** sind und es **keine verwaisten Datensätze** gibt.

Ein Fremdschlüssel ist ein **Feld** oder eine **Gruppe von Feldern** in einer Tabelle, die auf den [[Primärschlüssel]] einer anderen Tabelle verweist.
Er wird verwendet, um eine **Beziehung** zwischen den beiden Tabellen herzustellen, so dass Daten aus einer Tabelle auf der Grundlage von Daten in der anderen Tabelle abgerufen werden können.

___

## Ein Beispiel:

Nehmen wir zum Beispiel an, wir haben zwei Tabellen: 

- "Kunden"
- "Bestellungen". 

Die Tabelle "Kunden" hat einen <mark style="background: #D2B3FFA6;">Primärschlüssel "customer_id"</mark> und die Tabelle "Bestellungen" hat einen <mark style="background: #BBFABBA6;">Fremdschlüssel "customer_id"</mark>, der auf den Primärschlüssel der Tabelle "Kunden" **verweist**.
Dadurch wird eine **Beziehung zwischen den beiden Tabellen** hergestellt, so dass wir alle Bestellungen für einen bestimmten Kunden abrufen können, indem wir die customer_id als **Link** verwenden.

___

## Fremdschlüssel und Datenintegrität

Fremdschlüssel tragen auch dazu bei, die Datenintegrität zu gewährleisten, indem sie **Einschränkungen der referentiellen Integrität** erzwingen, die Folgendes umfassen können:

- **Einschränken:** Verhindert das Löschen eines Datensatzes, der von einem Fremdschlüssel referenziert wird.
- **Null setzen:** Setzt den Wert des Fremdschlüssels auf Null, wenn der referenzierte Datensatz gelöscht wird.
- **Setze Standard:** setzt den Wert des Fremdschlüssels auf den Standardwert, wenn der referenzierte Datensatz gelöscht wird.

___

## Zusammenfassung

Fremdschlüssel sind ein grundlegendes Konzept in relationalen Datenbanken. Sie ermöglichen die **Verknüpfung von Daten über Tabellen hinweg** und machen Datenbanken **effizienter** und **konsistenter**.


