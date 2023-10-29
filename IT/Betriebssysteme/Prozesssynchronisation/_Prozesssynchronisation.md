# Prozesssynchronisation

#prozesssynchronisation

### Mehrere Bedeutungen!

* Angleichen von Echtzeituhten in **verteilten Systemen**
* Abgleichen von **Daten** in ebendiesen
* Gleichzeitiges Abspielen von Ton- und Videodateien
* Generell: ***Koordination des zeitlichen Ablaufs von Prozessen***
* ...

### Funktionsablauf

Ein **Prozess** wartet auf ein Ereignis, auf das Eintreten einer Bedingung. Während des Wartens **schläft** ebendieser Prozess (Ausnahme: [[Busy Waiting]])
Das Betriebssystem weckt den Prozess, wenn Bedingung als erfüllt betrachtet.

