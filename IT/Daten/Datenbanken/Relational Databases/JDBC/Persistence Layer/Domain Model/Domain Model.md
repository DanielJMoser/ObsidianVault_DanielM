
**Software besteht aus:**
- Applikationsspezischen Code (Business Logic)
- Technologiespezifischen Code (JDBC, Hibernate, ...)

## Separations of Concerns

Dabei sind die beiden **stets zu separieren!** So kann technologiespezifischer Code ausgetauscht werden, ohne den applikationsspezifischen anfassen zu müssen.

___

## Domain Model – Definiert

Das Domain Model beschreibt, wie die **Geschäftslogik** in einer Anwendung **organisiert und modelliert** wird. 
Es ist eine Art **Blaupause** oder **Entwurfsmuster**, das die wesentlichen Geschäftsobjekte und die Beziehungen zwischen ihnen beschreibt.

Ein Domain Model kann zum Beispiel die [[Entity]] einer Online-Shopping-Anwendung beschreiben, wie Kunden, Bestellungen, Produkte und Zahlungen, sowie die **Beziehungen** zwischen ihnen, wie eine Bestellung, die einem Kunden zugeordnet ist, oder ein Produkt, das zu einer Bestellung gehört.

Das Domain Model wird oft in einer **UML-Diagramm** oder einer anderen grafischen Notation dargestellt. Es bildet die Grundlage für die Entwicklung des restlichen Systems und wird verwendet, um die Anforderungen an die Software zu verstehen und umzusetzen.

___

## Zwei Arten

- [[Rich Domain Model]]
- [[Anemic Domain Model]]



