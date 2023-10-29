-> Konzept aus der **Softwareentwicklung**, das eng mit dem [[Domain Model]] verwandt ist. 

Es beschreibt eine **Design-Strategie**, bei der die Geschäftslogik der Anwendung in den Kernobjekten ([[Entity|Entitäten]]) des Domain Models implementiert wird, anstatt sie in separaten Dienst- oder Serviceklassen zu kapseln.

Das Rich Domain Model ist insofern "**reichhaltig**", als es nicht nur die

- **Eigenschaften** und 
- **Beziehungen** 

zwischen den Objekten beschreibt, sondern auch die **zugehörige Geschäftslogik** enthält. 

Die Objekte im Domain Model sind also nicht nur "dumme" Datencontainer, sondern verfügen über Methoden, die die spezifischen Anforderungen des Systems implementieren.

___

## Beispiel

Ein Beispiel für eine Anwendung mit einem Rich Domain Model könnte eine Online-Banking-Anwendung sein, in der ein **Kontoobjekt** über Methoden verfügt, um 

- Überweisungen durchzuführen, 
- Kontostände abzufragen und 
- andere Banktransaktionen zu verarbeiten. 

Auf diese Weise kann das Domain Model direkt mit der **Benutzeroberfläche** kommunizieren und die Geschäftslogik auf eine strukturierte und leicht verständliche Weise implementieren.

Der Vorteil eines Rich Domain Models liegt darin, dass es die Entwickler in die Lage versetzt, die Geschäftslogik direkt in den Objekten des [[Domain Model]]s zu implementieren. 
Dadurch wird der Code **schlanker**, **kohärenter** und **leichter verständlich.** Außerdem können Tests einfacher durchgeführt werden, da die Geschäftslogik im Kontext des Domain Models isoliert getestet werden kann.
