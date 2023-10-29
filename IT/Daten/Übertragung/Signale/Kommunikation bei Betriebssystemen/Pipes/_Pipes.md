-> meist ein **Datenstrom** zwischen zwei Prozessen

(Unnamed) pipes sind ein Mechanismus zur **Interprozesskommunikation** (IPC) in Betriebssystemen. Sie ermöglichen es, Daten zwischen **zwei** Prozessen auszutauschen, ohne dass diese Prozesse direkt miteinander kommunizieren müssen.

Ein Pipe ist ein spezielles Dateiobjekt, das erstellt wird, wenn ein Prozess den Befehl `pipe` aufruft.
Es hat **zwei Enden**: 

* ein Lesende und ein 
* Schreibende. 

___

## Schreibende und lesende Prozesse

Der Prozess, der Daten in das Pipe schreibt, wird als **Schreibender Prozess** bezeichnet, während der Prozess, der die Daten aus dem Pipe liest, als **Lesender Prozess** bezeichnet wird.

Wenn der Schreibende Prozess Daten in das Pipe schreibt, werden diese Daten im **Pipe-Puffer** gespeichert. Der Lesender Prozess kann diese Daten dann aus dem Pipe lesen, wenn er bereit ist. Wenn der Puffer voll ist, wird der Schreibende Prozess **blockiert**, bis der Lesende Prozess Daten aus dem Pipe gelesen hat und Platz im Puffer frei geworden ist.

___

## Einschränkungen

Es ist wichtig zu beachten, dass ein Pipe nur für die Kommunikation zwischen Prozessen verwendet werden kann, die im **gleichen System** ausgeführt werden. 

**_Unnamed Pipes sind nicht für die Kommunikation zwischen Prozessen auf entfernten Systemen geeignet._**

Für diesen Anwendungsfall ist auf die [[Named Pipes]] zu verweisen.

