# Inkorrekter Prozessablauf

#prozesssynchronisation


## Zusammenfassung

* Ein Ablaufplan muss so designed werden, dass jeder Ausführungspfad ein **valides Endergebnis** produziert!
* Ein Ablaufplan muss so designed werden, dass [[_Deadlock|Deadlocks]] entweder **komplett vermieden** werden, oder das System nur [[Sichere Zustände]] annehmen kann!
* Kein Zyklus im Ablaufplan darf zum [[Livelock]] führen!
* Der zeitliche Ablauf muss **wohldefiniert** sein, d.h. [[Race Conditions]] müssen **ausgeschlossen** sein!
* Der Ablaufplan muss Ressourcen [[Starvations#^fairness|fair]] verteilen, sodass [[Starvations]] nicht auftreten können!

Ein Beispiel eines problematischen Ablaufs ist das [[Dining Philosophers Problem]]!