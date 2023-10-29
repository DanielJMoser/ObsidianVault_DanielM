
Der Rückwärtspropagationsprozess berechnet die **Gradienten der Verlustfunktion** im Hinblick auf die **Gewichte und Bias-Werte** des neuronalen Netzwerks. 
Diese Gradienten werden anschließend verwendet, um die Gewichte und Bias-Werte in einer Weise **anzupassen**, die den Verlust **minimiert**. Dieser Prozess ermöglicht das Lernen des Netzwerks.

#### Formel

$\frac{\partial Loss}{\partial w_{ji}^h} = \frac{\partial Loss}{\partial a_j^h} \cdot \frac{\partial a_j^h}{\partial z_j^h} \cdot \frac{\partial z_j^h}{\partial w_{ji}^h}$

- $\frac{\partial Loss}{\partial w_{ji}^h}$ -> Der Gradient des Verlusts nach dem Gewicht ${\partial w_{ji}^h}$
- $\frac{\partial Loss}{\partial a_j^h}$ -> Der Gradient des Verlusts nach der Ausgabe des Neurons $\partial a_j^h$
- $\frac{\partial a_j^h}{\partial z_j^h}$ -> Der Gradient der Aktivierungsfunktion nach dem gewichteten Summenwert ${\partial z_j^h}$
- $\frac{\partial z_j^h}{\partial w_{ji}^h}$ -> Der Gradient des gewichteten Summenwerts nach dem Gewicht ${\partial w_{ji}^h}$

# Bedeutung

Die [[Forward Propagation]] berechnet die **Vorhersagen** des Modells basierend auf den aktuellen **Gewichten** und **Bias-Werten**. 
Die [[Backpropagation]] berechnet dann die **Gradienten**, die anzeigen, **wie stark** und **in welche Richtung** die Gewichte und Bias-Werte angepasst werden müssen, um den Verlust zu minimieren. 
Die Backpropagation nutzt die **Kettenregel** der Ableitung, um den Einfluss der Gewichte auf den Verlust rückwärts durch das Netzwerk zu propagieren.