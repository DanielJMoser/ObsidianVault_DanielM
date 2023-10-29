

Bewegt sich **mehr als ein** Programm im selben Speicherbereich, so ergeben sich diverse Probleme. So müsssen diese etwa

- an **verschiedenen Stellen** im Speicher geladen werden,
- **Sprungadressen** stimmen nicht mehr
- Globale Variablen befinden sich ev. an der **falschen Stelle**

Da zum Zeitpunkt des Kompilierens/Linkens nicht bekannt ist, an welcher Stelle im Speicher das Programm geladen wird, ergibt sich das sogenannte [[Relokationsproblem]].
