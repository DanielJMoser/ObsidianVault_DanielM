# Deadlock

#prozesssynchronisation
#deadlock

siehe -> [[Dining Philosophers Problem]]

zu Deutsch -> Verklemmung

**Mehrere Prozesse sind in einem Zustand gefangen!**
Hier verharren die Prozesse **für immer** in selbigem Zustand. Im Gegensatz hierzu: [[Livelock]]

________

## Vier notwendige Kriterien:

##### Mutual Exclution:
Der Zugriff auf Betriebsmittel ist exklusiv (Zugriff nur einer Partei gestattet!)

##### Hold and Wait
Die Prozesse fordern Betriebsmittel an, behalten aber gleichzeitig den Zugriff auf andere

##### No Preemption
Die Betriebsmittel werden ausschließlich durch die Prozesse freigegeben

##### Circular Wait
Mindestens zwei Prozesse besitzen bezüglich der Betriebsmittel eine zirkuläre Abhängigkeit

___

## Wie vermeide ich Deadlocks?

-> [[Deadlock Avoidance]]
-> [[Deadlock Prevention]]

Sollte ein Deadlock dennoch eintreten:
-> [[Deadlock Recovery]]

