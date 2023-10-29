Während der Vorwärtspropagation durchläuft eine Eingabe (oft als **Eingabevektor** oder **Eingabematrix** bezeichnet) das neuronale Netzwerk, Schicht für Schicht, von der **Eingabeschicht** bis zur **Ausgabeschicht**. 
Jede Schicht besteht aus **Neuronen** oder Knoten, die mit Gewichten und **Aktivierungsfunktionen** verbunden sind. 

## Formel

Für eine 
- versteckte Schicht **h** mit Neuronen **i** und 
- Ausgabeschicht **o**  mit Neuronen **j**:

$$a_j^h = \Sigma_i(w_{ji}^h * a_i^{h - 1}) + b_j^h$$
$$a_j^h = Aktivierungsfunktion(a_j^h)$$

# Bedeutung

Die [[Forward Propagation]] berechnet die **Vorhersagen** des Modells basierend auf den aktuellen **Gewichten** und **Bias-Werten**. 
Die [[Backpropagation]] berechnet dann die **Gradienten**, die anzeigen, **wie stark** und **in welche Richtung** die Gewichte und Bias-Werte angepasst werden müssen, um den Verlust zu minimieren. 
Die Backpropagation nutzt die **Kettenregel** der Ableitung, um den Einfluss der Gewichte auf den Verlust rückwärts durch das Netzwerk zu propagieren.

