-> Art des [[_Machine Learning|Maschinellen Lernens]]

Der Algorithmus wird mit **beispielhaften Inputs und Outputs** und deren **Verbindungen untereinander** gefüttert und soll **allgemeine Regeln** lernen, welche Inputs mit Outputs verknüpfen. Er wird so lange trainiert, bis das gewünschte Level an Genauigkeit erreicht wird. Für alle Elemente der Trainingssatzes ist eine Lösung, ein sog. **Label** vorhanden.

# Anwendungsfälle

Die häufigsten Anwendungsfälle sind

### Classification

Inputs werden in **zwei oder mehr Klassen** eingeteilt. Der Algorithmus muss unbekannte Inputs in eine oder mehrere dieser Klassen einteilen. Dabei unterscheidet man zwischen **binary** und **multiclass classification**.  -> Vorhersag diskreter Klassen, im Gegensatz zur [[Supervised Learning#Regression|Regression]]

![[zzDrawing_Classification.png]]

### Regression

Extrapoliert einen **numerischen Wert** in die Zukunft. -> Vorhersage stetiger Werte, im Gegensatz zur [[Supervised Learning#Classification|Klassifikation]]


![[zzDrawing_Regression.png]]

## Beispiele

- Image Classification
  -> Es wird mit Bildern und Labels gearbeitet. Der Algorithmus soll im Endeffekt in der Lage sein, neue Bilder richtig zu erkennen.
- Market Prediction/Regression
  -> Der Computer wird mit historischen Daten der Aktienmarktes gefüttert und soll daraus zukünftige Preisentwicklungen schließen.


