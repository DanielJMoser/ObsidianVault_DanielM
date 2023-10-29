-> eine Art von [[Supervised Learning|überwachtem Lernalgorithmus]] im Machine Learning.
Sie werden hauptsächlich für **Klassifikations**- und **Regressionsaufgaben** verwendet. SVMs sind besonders nützlich, wenn es darum geht, eine **Trennlinie oder -fläche** zwischen Datenpunkten unterschiedlicher Klassen zu finden.

Die grundlegende Idee hinter SVMs ist es, eine Trennlinie (oder eine Trennhyperebene in höheren Dimensionen) zu finden, die den **Abstand** zwischen den nächstgelegenen Datenpunkten verschiedener Klassen maximiert. Diese nächstgelegenen Datenpunkte werden als "Support Vectors" bezeichnet, da sie maßgeblich zur Definition der Trennlinie beitragen.

Hier sind einige Schlüsselkonzepte von SVMs:

1. **Margin**: Der Abstand zwischen der Trennlinie und den nächsten Datenpunkten (Support Vectors) wird als Margin bezeichnet. SVMs streben danach, eine Trennlinie zu finden, die den Margin maximiert, um eine bessere Generalisierung auf neue Daten zu ermöglichen.
    
2. **Hyperplane**: In einem zweidimensionalen Raum ist eine Trennlinie eine Linie, die Datenpunkte verschiedener Klassen voneinander trennt. In höherdimensionalen Räumen spricht man von einer Trennhyperebene.
    
3. **Kernel-Trick**: SVMs können auch auf nichtlineare Trennungen erweitert werden, indem ein Kernel-Trick angewendet wird. Der Trick besteht darin, die Daten in einen höherdimensionalen Raum abzubilden, in dem sie möglicherweise linear trennbar sind, obwohl sie in ihrem ursprünglichen Raum nicht linear trennbar sind.
    
4. **C-Konstante**: Die C-Konstante in SVMs beeinflusst das Trade-off zwischen der Erzielung eines größeren Margins und der Minimierung von Klassifikationsfehlern auf dem Trainingsdatensatz. Ein kleinerer Wert von C legt mehr Gewicht auf das Erzielen eines größeren Margins, während ein größerer Wert von C mehr Gewicht auf die Minimierung von Klassifikationsfehlern legt.

![[zzDrawing_SVM]]

SVMs werden in verschiedenen Anwendungen eingesetzt, darunter Textklassifikation, Bilderkennung, Bioinformatik, Finanzanalyse und mehr. Sie bieten eine effektive Methode zur Lösung von Klassifikations- und Regressionsproblemen, insbesondere wenn die Datenpunkte nicht linear separierbar sind.

