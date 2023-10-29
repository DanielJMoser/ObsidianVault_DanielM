# Starvations
#prozesssynchronisation 

-> die **Ressourcenaforderung kann nie vollständig erfüllt**, also auch die Aufgabe nicht positiv abgeschlossen werden.


So führt jeder [[_Deadlock|Deadlock]] sowie jeder [[Livelock]] zur Starvation der beteiligten Prozesse.

Eine weitere Ursache sind oftmals zu simple **Scheduling-Algorithmen/Ablaufpläne**. Kommt es nicht zur Starvation, so spricht man von **Fairness** bzw. **"Ein Algorithmus ist fair"**. ^fairness

___

## Starving Philosopher's Problem

-> mögliche Lösung des [[Dining Philosophers Problem]]!

So greift man bei 

![[Dining Philosophers Problem#^da9500]]


ein und tauscht den Befehl gegen folgendes Kommando aus:


>3. Wenn rechte Gabel nicht verfügbar, gebe linke Gabel ab, denke eine zufällige Zeit lang nach und gehe wieder zu Schritt 2.

Die Philosophen warten für einen **zufälligen Zeitraum** also wahrscheinlich **unterschiedlich lang**! So ist sichergestellt, dass nicht alle Philosophen gleichzeitig essen wollen -> sonst: [[Livelock]]!
Ein Deadlock ist nicht mehr möglich, da das [[_Deadlock#Hold and Wait|Hold and Wait]]-Kriterium nicht erfüllt ist.


### Pechvogel: Eine Problematik

Angenommen, die Philosophen sind so hungrig, dass sie dauernd essen wollen.

Während alle Anderen eine recht **kurze** Wartezeit ziehen, muss Philosoph *P* immer **lange** warten. Während der Pechvogel noch versucht, eine Gabel zu erhaschen, essen die Anderen bereits wieder. 

Philosoph P wird also **niemals** eine Gabel erhalten und elendiglich verhungern, der Arme! -> ***Starvation**

___

## Vermeidung von Starvations

Wie schon bei [[_Deadlock|Deadlocks]] ist kein "Universalrezept" bekannt, um Starvations zu vermeiden!

Zur Prävention müssen Scheduling-Algorithmen und Ablaufpläne [[Starvations#^fairness|fair]] designed werden. Nachträglich lassen sie sich nur schwer ausbessern, eine Auflösung beim Eintreten ist **praktisch unmöglich**!


