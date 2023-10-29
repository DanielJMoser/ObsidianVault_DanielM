# Binäre Suche

## Grundidee

- Um einen **Wert x** in einem **Array A** zu finden, starte in der Mitte von A.
- Falls x = A[n/2] -> **fertig**, x (welches die Mitte des Arrays bildet) wurde gefunden.
- Falls x < A[n/2] -> gehe zu Punkt 1 mit A[0: [n/2]] -> wir müssen in der **linken Hälfe** des Arrays suchen.
- Falls x > A[n/2] -> gehe zu Punkt 1 mit A[[n/2] + 1 : n - 1] -> wir werden in der **rechten Hälfte** des Arrays fündig werden.


