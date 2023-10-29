## Konvertieren

$-2,5 \times 10^{-2} \to −0,025$.

- Ganzzahliger Teil: $0$ -> auch im Binärsystem!
- Dezimaler Teil: $0,025$ -> muss behandelt werden.
### Nachkommastellen

...wie gehabt...
$$
\begin{align}
−0,025×2=−0,05 (0) \\
−0,05×2=−0,1 (0) \\
−0,1×2=−0,2 (0) \\
−0,2×2=−0,4 (0) \\
−0,4×2=−0,8 (0) \\
−0,8×2=−1,6 (1) \\
−0,6×2=−1,2 (1) \\
\\
−0,2×2=−0,4 (0) \\
−0,4×2=−0,8 (0) \\
−0,8×2=−1,6 (1) \\
−0,6×2=−1,2 (1) \\
\end{align}
$$... und so weiter. 
An dieser Stelle sehen wir, dass sich der Prozess **wiederholen** wird, sobald wir bei $-0,2$ angelangen.
-> **periodische** Nachkommazahl

## Normalisierte Wissenschaftliche Notation

Nun muss unsre Zahl in die **normalisierte wissenschaftliche Notation** umgewandelt werden. 
In dieser hat eine binäre Gleitkommazahl die Form:
$$ (-1)^{s} \times 1, f \times 2^{e} $$
...wobei:

- $s$ das **Vorzeichenbit** ist (*0* für positive Zahlen, *1* für negative Zahlen),
- $f$ die **Mantisse** (Fraction) ist, die eine *binäre Dezimalzahl* darstellt, und
- $e$ der **Exponent** ist, der die *Potenz von 2* angibt, mit der multipliziert wird. Dieser ist hier schon um den **Bias** korrigiert!

Um die Zahl $-0,000011$ in die normalisierte wissenschaftliche Notation umzuwandeln, verschieben wir das Komma nach **rechts**, bis es direkt **hinter** der ersten 1 steht. 

Jeder Schritt nach **rechts** entspricht einer **Division**.
Jeder Schritt nach **links** entspricht einer **Multiplikation**.

-> nach **6** Schritten: $−0,0000011001100110011…=−1,1001100110011…×2^{−6(unkorrigiert)}$

### Berechnung des Exponenten und Mantisse

- Da negative Zahl -> Vorzeichenbit ist **1**
- Bias für einfache Genauigkeit: **127**
  $127 - 6 = 121$
  - 121 in binärer Darstellung mit 8 Bits:
    $01111001$
- Die Mantisse ist die binäre Darstellung der Zahl nach dem Binärpunkt. In der IEEE 754 Darstellung -> **23 Bits** lang!

| $s$ | $e$ | $f$ |
| -------- | -------- | -------- |
| 1 | 01111001 | 10011001100110011001100 |

