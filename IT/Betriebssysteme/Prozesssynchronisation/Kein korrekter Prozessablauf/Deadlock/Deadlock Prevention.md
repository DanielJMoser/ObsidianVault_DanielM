# Deadlock Prevention
#prozesssynchronisation
#deadlock 

**Mindestens eine** der [[_Deadlock#Vier notwendige Kriterien|Kriterien zum Deadlock]] trifft nicht mehr zu, womit ein solcher theoretisch nicht mehr eintreten kann.

* **[[_Deadlock#Mutual Exclution|Mutual Exclution]] beseitigen** (z.B. Druckerwarteschlange, Spooling)
* **[[_Deadlock#Hold and Wait|Hold and Wait]] verhindern** (z.B. Freigabe noch belegter Ressourcen anstatt zu warten)
* **[[_Deadlock#No Preemption|No Preemption]] durchführen** (Belegte Ressourcen können unfreiwillig wieder entzogen werden -> Mittelmann haut den [[Dining Philosophers Problem|Philosophen]] auf die Finger)
* **[[_Deadlock#Circular Wait|Circular Wait]] ausschließen**(geeignetes Vergabeverfahren verwenden, sodass keine zirkuläre Abhängigkeiten entstehen)
