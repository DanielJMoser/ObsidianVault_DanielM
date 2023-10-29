# Race Conditions
#prozesssynchronisation 


## Race Condition

-> Situation, in der das Ergebnis einer Operation vom **zeitlichen Verhalten bestimmter Einzeloperationen** abhängt.

Angenommen, es existiert eine **Globale Variable A** und **zwei paralell laufende Threads**, welche jeweils **unterschiedliche Werte** in A speichern.

![[zzDrawing_Race-Condition.png]]



##### Was wird am Ende ausgegeben?

-> Der **zuletzt gespeicherte** bzw. der **langsamere** Wert!
-> Unterschiedliches zeitliches Verhalten sorgt für unterschiedliche Ergebnisse.

Da die [[Threads|Threads]] parallel ausgeführt werden, ist ihre Reihenfolge nicht deterministisch, ergo zufällig! So wird beim einen Mal Thread 1 schneller, mal Thread 2 schneller sein.

Aufgrund **zunehmender Parallelisierung**[^1] tritt eine solche Situation immer häufiger auf, was sich unter Umständen schwerwiegend auf das System einwirkt.

Da diese zufällig auftreten, sind sie **nicht leicht reproduzierbar** und damit beim Debugging nur sehr umständlich aufzufinden, beim Auftreten in größeren Projekten **quasi unmöglich**! [^2]


***Prävention*** durch möglichst umfassende **Modellierung** im Vorfeld, achtsamer Implementierung! 





____

[^1]: (ausgelöst durch leistungsstärkere, größere Prozessoren mit immer zahlreicheren Kernen und demnach auch Threads, anm.)

[^2]:  (Bei meinem Glück läuft's 99x glatt, beim 100sten Mal geht's dann erst schief)





