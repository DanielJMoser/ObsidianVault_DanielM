# Semaphor
#Datenstrukturen 
#synchronisationsprimitiven 
#prozesssynchronisation 

Hierbei handelt es sich um eine [[_Datenstrukturen|Datenstruktur]], bestehend aus
* Einer Ganzzahl (i.d.R. mit Wert <0 initialisiert)
* Der Operation *down()* bzw. *wait()*
* Der Operation *up()* bzw. *post()*

## Down()

-> **Überprüft** den Wert des Semaphors!

* Wenn < 0, wird der Wert um 1 **reduziert**.
* Wenn > 0, wird **gewartet** bis der Wert wieder größer als 0 wird – dann um 1 reduziert

## Up()

-> **Erhöht** Wert um 1


___

Damit können [[Kritische Regionen]] beschützt werden! Beim Eintritt in dieselbe wird *down()* aufgerufen. Während der Prozess sich darin befindet, ist der Wert **gleich Null**. Beim Austritt wird *up* gecalled.

Wird der Semaphor etwa mit **2** initialisiert, so können **zwei Prozesse** in die [[Kritische Regionen|Kritische Region]] eintreten.

___

## Unterschiedliche APIs

-> ***ACHTUNG:*** für Semaphore existiert mehr als eine API!

Neben der **POSIX**-API existiert etwa noch die**System V**-API. Bei der Codejagd im Netz zu beachten!

-> Sephamore sind nicht das einzige Beispiel, wo es mehr als eine Betriebssystem-API gibt.