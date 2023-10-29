								# AVL-Bäume
-> nach  Georgy **A**delson-**V**elsky und Evgenii **L**andis (1962)

Die Höhe jedes Knotens muss **im Knoten gespeichert** werden!

## Berechnung d. Höhenunterschieds

$$\mathcal{diff = Höhe(linker Unterbaum) - Höhe(rechterUnterbaum)}$$


- Höhenunterschied **beschränkt** auf [-1; 0; +1]!

- Für **Blätter** gilt: $$\mathcal{diff = 0}$$
Vier verschiedene Arten von [[Rotation|Rotationen]], welche sich nach dem **Einfügen/Löschen** notwendig machen.

------------

## Insert bei AVL-Bäumen

- Suche Knoten, an den **neues Blatt angehängt** werden soll.
- An diesem Knoten ändert sich die Höhe und damit die **Höhendifferenz um ±1** (linkes oder rechtes Blatt).
- Gehe nun rückwärts (rekursiv) zur Wurzel, aktualisiere die **Höhen und Höhendifferenzen** und falls nötig **rotiere den (Unter)Baum.
- Falls Höhendifferenz ±2 ist, ist entweder **Einfach- oder Doppelrotation** erforderlich.

-----------------------------

## Delete bei AVL-Bäumen

- Suche Knoten v , der gelöscht werden soll.
- Falls V ein **Blatt** ist, oder **genau ein Kind** hat, _lösche_ bzw. _ersetze_ v durch sein Kind und aktualisiere Höhe des Vaterknotens -> **rekursiv bis zur Wurzel der anderen Knoten.**
- Falls v 2 Kinder hat, vertausche v mit dem **Minimum des rechten Teilbaums** (wie beim BST) und lösche v dort. Dort hat v höchstens ein Kind.
- Falls Höhendifferenz ±2 ist , ist **entweder Einfach- oder Doppelrotation** erforderlich.
- Falls notwendig, Höhendifferenz des Vaters nach Rotation anpassen und ggf weiter rotieren.

