# Mutex
#Datenstrukturen 
#synchronisationsprimitiven 
#prozesssynchronisation 

-> vereinfachte [[Semaphor]], welche **nur mit 1** initialisiert werden kann. Abkürzung für **Mutual Exclusion**, hauptsächlich zum Schutz von Regionen verwendet.

**Zwei Operanden**: *lock()* und *unlock()*

Ist ein Mutex bereits gesperrt, dann wird der nächste *lock()*-Aufruf so lange gesperrt, bis *unlock()* gecalled wird.