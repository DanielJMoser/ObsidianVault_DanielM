# Zustandsvariable
#Datenstrukturen 
#synchronisationsprimitiven 
#prozesssynchronisation 

-> Kann benutzt werden, um einen Prozess oder Thread so lange zu blockieren, bis **ein bestimmtes Ereignis eingetreten** ist.

**Zwei Operanden**: *wait()* und *signal()*

* **wait()** blockiert den aufrufenden Prozess so lange, bis ein Ereignis eingetreten ist.
* **signal()** wird dazu verwendet, um den wartenden Prozess das Eintreten des Ereignisses mitzuteilen.

## Beschützende Mutex

Müssen immer durch eine [[Mutex]] beschützt werden!
