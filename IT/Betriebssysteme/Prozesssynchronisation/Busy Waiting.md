# Busy Waiting
#prozesssynchronisation 

-> eine Technik, bei der ein Prozess auf ein **bestimmtes Ereignis wartet**, indem es immer wieder überprüft wird, ob das Ereignis eingetreten ist. 

Dies führt zu einer **hohen CPU-Auslastung**, da der Prozess keine Zeit zur Verfügung hat, um andere Aufgaben auszuführen, während er wartet.
Busy Waiting ist in der Regel **ineffizient** und sollte **vermieden** werden, wenn möglich, indem man stattdessen auf **Interrupts** oder [[_Signale|Signale]] wartet.