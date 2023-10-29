#BigData 
-> Bei [[Stream-based data processing]]

Stream Operations sind **Funktionen**, die auf Datenströmen angewendet werden können, um sie zu transformieren oder zu filtern. Die meisten Stream Operations können auf einzelnen Elementen eines Datenstroms angewendet werden oder die Elemente eines Datenstroms aggregieren.

Es gibt zwei Arten von Stream Operations: **intermediate** und **terminal**. 
**Intermediate** Stream Operations werden auf Datenströmen angewendet, um sie zu transformieren oder zu filtern und geben einen neuen Stream zurück.
**Terminal** Stream Operations hingegen führen eine abschließende Operation auf dem Datenstrom aus und geben ein Ergebnis zurück.

## Welche Stream Operations gibt es?

Es gibt viele verschiedene Arten von Stream Operations, darunter:

-   **map()**: wendet eine Funktion auf jedes Element des Datenstroms an und gibt einen neuen Datenstrom zurück, der die Ergebnisse enthält.
-   **filter()**: filtert Elemente aus dem Datenstrom heraus, die bestimmte Kriterien erfüllen, und gibt einen neuen Datenstrom zurück, der nur die verbleibenden Elemente enthält.
-   **reduce()**: aggregiert die Elemente des Datenstroms auf eine einzige Ausgabe.
-   **collect()**: sammelt die Elemente des Datenstroms in einer Liste oder einem anderen Sammelobjekt.
-   **distinct()**: gibt nur eindeutige Elemente des Datenstroms zurück.
-   **sorted()**: sortiert die Elemente des Datenstroms.

## Verwendung von Stream Operations

Stream Operations werden häufig in der Verarbeitung von Datenströmen in [[Echtzeitsysteme|Echtzeit]] verwendet, z. B. bei der Analyse von Log-Dateien, Sensor-Daten oder Finanzdaten. 
Sie sind auch in der [[_Big Data|Big-Data-Verarbeitung]] nützlich, um große Datenmengen in Echtzeit zu analysieren und zu verarbeiten.

Stream Operations können in **verschiedenen Programmiersprachen** verwendet werden, darunter Java, Python und Scala. 
Sie können auch in **Stream-Processing-Frameworks** wie Apache Kafka, Apache Storm und Apache Flink verwendet werden, die speziell für die Verarbeitung von Datenströmen entwickelt wurden.