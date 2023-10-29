# Ereignisorientierte Programmierung
#embeddedsystems 
#paradigmen 

Oft bei [[_Embedded Systems|Embedded Systems]] zu finden!

Hierbei wird **kein lineares, von oben nach unten durchlaufendes** Programm geschrieben. Stattdessen werden bei Eintritt eines Ereignisses sogenannte **Event Handler** aktiv.

----------------------------------------

## Inversion of Control

-> **Hauptkontrollfluss** wartet <mark style="background: #FF5582A6;">nicht mehr</mark> auf das Eintreten eines Ereignisses! -> Jedes Ereignis erzeugt stattdessen einen **eigenen Kontrollfluss**.

Auch **Mischformen**, bei dem ein lineares Hauptprogramm normal Befehle ausführt und von Ereignissen via [[Exception Handling]] unterbrochen wird, sind in der Praxis häufig anzutreffen.

---------------------

## Interrupts

-> Auf unterster Ebene anzutreffen, hardwareimplementiert.

Diese **unterbrechen** den momentanen Programmfluss und **springen** zu einer gegebenen **Befehlsaddresse**.
Sie sind **konfigurierbar** und damit **ein- und ausschaltbar**.

Anwendungsfälle wären etwa die *Division durch Null*, die *Verfügbarkeit von Daten* (durch Abschluss einer [[Analog-Digital-Wandler|ADC]]-Umwandlung) oder die *Veränderung von I/O-Pins*.

Dabei wird ein Programm normal ausgeführt. Löst der Interrupt aus, so wird an **exakt dieser Stelle** (überall möglich!) unterbrochen. Indem man Interrupts global **aus- und dann wieder anschaltet** (*cli()* und *sei ()*) werden, können kritische Stellen **geschützt** werden.
Die **Interrupt Service Routine** wird ausgeführt, möglichst rasch wieder beendet und das Programm weiter ausgeführt.

