# Echtzeitsysteme
#embeddedsystems 

-> [[Eigenschaften ES#Echtzeitsysteme Echtzeitfähigkeit bei Embedded Systems|Definition Echtzeitsysteme]]


Grobe Unterscheidung: **Harte** und **Weiche Echtzeitsysteme**!


## Harte Echtzeitsysteme
* Definierte Reaktionszeit wird **niemals** überschritten!
* Nichteinhaltung birgt oft **gravierende Sicherheitsrisiken**
* Sicherheitssysteme fallen i.d.R. immer in diese Kategorie (z.B. Airbag, Herzschrittmacher,...).

_Harte Echtzeit_ kann nur **mathematisch** bewiesen werden! 

Bei [[Zeitgesteuerte Systeme|zeitgesteuerten Systemen]] wird die max. Reaktionszeit aus dem **bekannten Zeitplan** und der **Bearbeitungszeit d. Ereignishandlung** berechnet.

Bei [[Ereignisgesteuerte Systeme|Ereignisgesteuerten Systemen]] hingegen setzt sie sich aus der Zeit bis zum **Auslösen des** [[Entwicklung von ES#Interrupts|Interrupts]] und der **Laufzeit der Service Routine** zusammen.

Es wird vom <mark style="background: #FF5582A6;">Worst-Case-Scenario</mark> ausgegangen.



## Weiche Echtzeitsysteme
* Reaktionszeit wird **statistisch** erreicht, es gibt also Ausreißer.
* Nichteinhaltung birgt nur **kleine Unannehmlichkeiten.**
* Etwa **Unterhaltungssysteme** (brechen Bild und Ton kurzzeitig ab, befinden sich keine Menschen in unmittelbarer Gefahr) fallen in diese Kategorie.

_Weiche Echtzeit_ wird durch **statistische Auswertung** bewiesen!


### Zwei Paradigmen:

* [[Zeitgesteuerte Systeme]]
* [[Ereignisgesteuerte Systeme]]

------------------------------------

