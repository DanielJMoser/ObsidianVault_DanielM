# Bus-Systeme
#embeddedsystems
#kommunikationsnetzwerke

-> Art eines [[_Kommunikationsnetzwerke|Kommunikationsnetzwerks]].

## Beispiele
* [[I²C]]
* **SPI**
* [[CAN-Bus]]

<mark style="background: #BBFABBA6;">Vorteile</mark> | <mark style="background: #FF5582A6;">Nachteile</mark> 
----------|---------
Effiziente Verkabelung | Nicht ohne Weiteres [[Echtzeitsysteme|echtzeitfähig]]
Effiziente Ressourcennutzung, da Pins von mehreren Partner_innen gemeinsam genutzt werden können. | Störung durch andere Partner_innen
 | Übertragungsleistung nicht immer effizient nutzbar |
 
**Dominant** in [[_Embedded Systems|eingebetteten Systemen]], aufgrund der effizienten Verkabelung und Ressourcennutzung. Nachteile können softwaretechnisch ausgeglichen werden:

* [[Echtzeitsysteme|Echtzeitfähigkeit]] durch entsprechende Protokolle
* Störungen werden durch etwa **Prüfsummen** oder **Access-Guards** vermieden.
* Verminderte Übertragungsleisung wird durch **Overprovisioning** ausgeglichen.

