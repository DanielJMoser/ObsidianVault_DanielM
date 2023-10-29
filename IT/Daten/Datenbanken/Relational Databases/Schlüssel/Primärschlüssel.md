
| CustomerID | Name       | Address      | Email          |
|:----------:| ---------- |:------------ |:-------------- |
|     1      | John Smith | 123 Main Str | john@smith.com |
|     2      | Jane Doe   | 456 Park Ave | jane@doe.com   |


In einer [[_Relationale Datenbanken|relationalen Datenbank]] ist ein Primärschlüssel ein **Feld** oder ein **Satz von Feldern**, der jeden Datensatz in einer Tabelle **eindeutig identifiziert**. Er wird verwendet, um die **Integrität der Daten** zu gewährleisten und sicherzustellen, dass es keine doppelten Datensätze in der Tabelle gibt.

Ein Primärschlüssel ist ein spezieller Typ eines _Kandidatenschlüssels_, d. h. er ist ein **eindeutiger Bezeichner** für die Zeilen der Tabelle. Jede Tabelle kann **nur einen Primärschlüssel** haben, der sich jedoch aus einer oder mehreren Spalten zusammensetzen kann.

___

## Einfache und zusammengesetzte Primärschlüssel

Ein Primärschlüssel kann entweder 

- **einfach** (bestehend aus einer einzigen Spalte) oder 
- **zusammengesetzt** (bestehend aus mehreren Spalten) 

sein. Einfache Primärschlüssel werden auch als **natürliche Schlüssel** bezeichnet. Sie verwenden einen **eindeutigen Bezeichner**, der bereits in den Daten vorhanden ist, z. B. eine Sozialversicherungsnummer oder eine **ID-Nummer** (wie in obigem Beispiel).
Zusammengesetzte Primärschlüssel werden verwendet, wenn sich der eindeutige Bezeichner aus **mehreren Spalten** zusammensetzt.

___

## Ein Beispiel:

Wir haben eine Tabelle mit dem Namen "Kunden" mit Informationen über Kunden wie **Name**, **Adresse** und **E-Mail**. Der Primärschlüssel könnte die **Kunden-ID** sein. Da keine zwei Kunden dieselbe ID haben, kann sie zur eindeutigen Identifizierung jedes Kunden in der Tabelle verwendet werden.

___

## Zusammenfassung

Zusammenfassend lässt sich sagen, dass ein Primärschlüssel ein **eindeutiger Bezeichner in einer relationalen Datenbanktabelle** ist. Er wird verwendet, um **Datenintegrität** zu erzwingen und doppelte Datensätze zu verhindern, er kann aus **einem oder mehreren Feldern** bestehen und er wird verwendet, um **Beziehungen** zwischen Tabellen herzustellen.