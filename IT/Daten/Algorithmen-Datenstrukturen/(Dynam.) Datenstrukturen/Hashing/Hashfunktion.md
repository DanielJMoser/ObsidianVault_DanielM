# Hashfunktion
-> Hauptbestandteil einer [[Hashtabelle]]

Bei **_gut umgesetzten_** Hashfunktionen beträgt die mittlere Dauer von Operationen konstant
$$\mathcal{O}(1)$$

## Wahrscheinlichkeit einer Kollision

Ergibt sich bei der Berechnung des Hashes ein Wert, welcher einen bereits **belegten** Platz in der Hashtabelle beschreiben würde, kommt es zur **Kollision**.

Die Wahrscheinlichkeit einer solcher wird wie folgt berechnet:

$$\mathcal{Pr(keine Kollision)} = {e} - \frac{n(n-1)}{2m}$$

Bei **steigendem n** steigt auch die **Wahrscheinlichkeit einer Kollision**.


