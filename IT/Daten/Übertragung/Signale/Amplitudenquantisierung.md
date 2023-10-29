# Quantisierung
#embeddedsystems

#### Quantisierungsfehler

Der **Quantisierungsfehler**... $$e_2$$ ...(auch *Quantisierungsabweichung* bzw. *Quantisierungsrauschen* genannt) ist die **Differenz** zwischen dem **Eingangssignal** und dem **Quantisierten Signal.**

$$-\frac{R_q}{2} < e_q \leqslant \frac{R_q}{2}$$
R(q) ......... Auflösung in Volt

---------------------------------------

### Weitere Fehler

* **Offsetfehler** -> Konstante Verschiebung d. quantisierten Signals.
  *Gegenmaßnahme*: Kalibration mit bekannter Spannung (ein Messpunkt ausreichend!)
* **Nichtlineare Fehler** -> Nicht konstante Verschiebung des quantisierten Signals.
  *Gegenmaßnahme*: Kalibration mit mehreren verschiedenen Messpunkten.
* **Elektromagnetische Interderent** anderer Bauteile
  *Gegenmaßnahme*: Sleep Mode!