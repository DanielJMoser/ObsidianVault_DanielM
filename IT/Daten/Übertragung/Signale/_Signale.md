# Signale
#embeddedsystems 

-> Darstellung einer Information durch eine **zeitveränderliche physikalische**, insbesondere **elektrische Größe** (z.B. Strom, Spannung, Feldstärke,...).
Diese wird durch einen **Parameter dieser Größe kodiert** (z.B. Amplitude, Phase, Frequenz, Impulsdauer,...).

--------------------------------------------------

#### Kontinuierliches Signal

* **Zeitkontinuierich**: Zu jedem Zeitpunkt ist ein Signalwert definiert.
* **Wertkontinuierlich**: Ein Signalwert kann einen beliebigen Wert annehmen (innerhalb der reelen Zahlen).


#### Diskretes Signal

* **Zeitdiskret**: Es ist nur für bestimmte, endlich viele Zeitpunkte ein Wert definiert.
* **Wertdiskret**: Ein Signalwert kann nur bestimmte, endlich viele Werte annehmen.


---------------------------------------------------

Ein [[_Mikrocontroller|Mikrocontroller]] kann nur **Zeit- und Wertdiskrete** Signale verarbeiten.

Kontinuierliche Signale weden daher ***diskretisiert*.**

Hierzu wird ein Signal in meist **gleichen Abständen** abgetastet und durch einen [[Analog-Digital-Wandler]] in einen **digitalen Wert** umgewandelt. -> Quantisierung

Siehe: [[Abtastung]]

___

Auch in [[_Signale bei Betriebssystemen]] werden Signale zur **Prozesskommunikation** verwendet.