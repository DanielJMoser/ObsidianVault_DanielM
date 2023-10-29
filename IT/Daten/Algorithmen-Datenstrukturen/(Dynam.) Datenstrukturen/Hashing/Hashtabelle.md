#Datenstrukturen 

-> [[_Datenstrukturen|Datenstruktur]] zur Speicherung von Key-Value-Paaren. Die Hauptkomponente ist dabei die [[Hashfunktion]], welche den **Speicherindex** berechnet.

# Warum Hash Tables?

Arbeitet man mit größeren Datenmengen, so stößt man bei Implementierungen mittels [[Arrays]] auf **Effizienzengpässe**. 
Im Gegensatz zu Arrays können Hashtabellen Daten in konstanter Zeit speichern und suchend abrufen.
Im Idealfall beträgt diese Zeit $$\mathcal{O}(1)$$

# Komponenten

- **Key**: Ein String oder Integer, welcher als Input einer [[Hashfunktion]] dient und den **Index** des zu speichernden oder zu suchenden Items angibt.
- [[Hashfunktion]]: Nimmt einen **Key** als Input an und gibt den sog. **Hash Index** zurück.
- **Hashtabelle**: [[_Datenstrukturen|Datenstruktur]], welche mittels [[Hashfunktion|Hashfunktionen]] Keys zu Values mappt