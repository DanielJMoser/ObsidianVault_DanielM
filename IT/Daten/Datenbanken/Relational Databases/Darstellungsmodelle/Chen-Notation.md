
Chen-Notation ist eine Methode zur graphischen Darstellung von [[ER-Modell|Entitäts-Beziehungs-Modellen]] (ER-Modelle) in der **Datenbankmodellierung**. 
Sie wurde von **Peter Pin-Shan Chen** in den 1970er Jahren entwickelt und ist eine der ältesten und am weitesten verbreiteten Methoden zur graphischen Darstellung von ER-Modellen.

___

## Darstellung

In der Chen-Notation werden <mark style="background: #D2B3FFA6;">Entitäten</mark> als <mark style="background: #D2B3FFA6;">Rechtecke</mark> dargestellt, wobei der Name der [[Entity]] in der **Mitte** des Rechtecks geschrieben ist. 
<mark style="background: #BBFABBA6;">Beziehungen</mark> werden durch <mark style="background: #BBFABBA6;">Pfeile</mark> dargestellt, die von einer Entität zu einer anderen zeigen, wobei das Ende des Pfeils mit einer **Kardinalitätsangabe** versehen ist, die die Anzahl der zugehörigen [[Entity|Entitäten]] beschreibt.

___

## Beispiel

Ein Beispiel für ein ER-Modell in der Chen-Notation könnte eine Darstellung einer **Bibliotheksdatenbank** sein, in der die Entitäten "**Buch**" und "**Autor**" dargestellt werden, die durch die Beziehung "**geschrieben von**" miteinander verbunden sind. 
In diesem Fall würde das ER-Modell ein Rechteck für die Entität "**Buch**" und ein Rechteck für die Entität "**Autor**" enthalten, die durch einen Pfeil mit einer Kardinalitätsangabe von "**eins zu viele**" (1:n) verbunden sind, die besagt, dass 

**_ein Buch von einem Autor geschrieben werden kann, aber ein Autor kann mehrere Bücher schreiben.**

___

Obwohl die Chen-Notation eine der **ältesten** und am **weitesten verbreiteten** Methoden zur graphischen Darstellung von ER-Modellen ist, gibt es auch andere Methoden wie die Notation von **Crow's Foot** oder die [[UML-Notation]] die verwendet werden können, um ER-Modelle darzustellen.