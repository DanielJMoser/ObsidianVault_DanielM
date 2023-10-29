# Entwicklung
#embeddedsystems

-> ***Kein großartiger Unterschied zur herkömmlichen Softwareentwicklung!*** (Wasserfall- und V-Modell, IDE, Versionsverwaltung,...)

Kleine Unterschiede, da andere **Optimierungsprioritäten** und Verwendung der Compilerflags -os statt -o2/-o3. Andere **Best Practices**, meist den begrenzten Ressourcen geschuldet.

--------------------------------------------------

## Wertabfragung

[[_Signale|Signale]] werden via **Polling** *(Zyklische Abfrage)* oder **Ereignissteuerung** via [[Ereignisorientierte Programmierung#Interrupts|Interrupts]] *(Programm wird bei Veränderung aktiv)* abgefragt.

[[_Embedded Systems|Embedded Systems]] müssen oftmals auf Ereignisse reagieren, daher:

-> [[Ereignisorientierte Programmierung]]

---------------------------


### Polling

<mark style="background: #BBFABBA6;">Vorteile</mark> | <mark style="background: #FF5582A6;">Nachteile</mark> 
-------------|-------
Braucht keine Hardware-Unterstützung | Oft nicht deterministisch 
Einfach umzusetzen | Ineffiziente Ressourcennutzung
Verursacht bei linearen Programmen wenig Overhead | 

-> [[Zeitgesteuerte Systeme]]


### Interrupts

<mark style="background: #BBFABBA6;">Vorteile</mark> | <mark style="background: #FF5582A6;">Nachteile</mark> 
-----------|---------
Effiziente Ressourcennutzung | Benötigt Hardware-Unterstützung
Deterministisch | Schwieriger umzusetzen
Verursacht in bei [[Ereignisorientierte Programmierung]] weniger Overhead |

-> [[Ereignisgesteuerte Systeme]]



