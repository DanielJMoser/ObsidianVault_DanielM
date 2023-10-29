# Paging

-> zum Einsatz kommende Technik bei [[Adressraum#Virtueller Speicher|Virtuellen Speichern]]

Hierbei besteht der 
* Virtuelle Adressraum aus **Einheiten fester Größe**, sogenannten **Seiten**, und dem
* Physische Adressraum aus **Einheiten fester Größe**, sogenannten **Seitenrahmen**.
* i.d.R. gleich groß!

*Für jeden Prozess:* individuelle Zuordnung von Seiten zu Seitenrahmen. Die Seiten werden also **"eingehängt"**.

___

## Demand Paging

-> Seiten werden erst eingehängt, **wenn tatsächlich benötigt**.
Speichersparende Technik! Wenig Overhead zu Beginn, welcher dann mit jedem Aufruf der Seite wächst.


## Prepaging

-> Seiten werden bereits eingehängt, **bevor sie benötigt** weden.
Neigt zur Speicherverschwendung! Viel Overhead zu Beginn, danach aber kaum.

