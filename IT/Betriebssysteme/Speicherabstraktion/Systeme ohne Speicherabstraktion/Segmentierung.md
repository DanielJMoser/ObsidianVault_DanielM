## Segmentierung

***-> Obsolet! Eigentlicher Sinn: Möglichkeit des Ansprechens von mehr als 64kb Speicher bei 16-Bit Systemen.***

-> **Single-Task-Systeme**

Ein Programm kann, bei fehlender Speicherabstraktion, auf den **gesamten** Speicher zugreifen -> **Sicherheitslücken!**

Um Speicher vor Malware zu schützen -> **Segmentierung**

Hierbei wird der Speicherraum in **Segmente** unterteilt, welchen jeweils ein **Segment-Deskriptor** zugeteilt wird. Dieser hat einen **Index** und speichert u.A. eine **Basis-Adresse** und eine **Größe**. Dieser wird im **Sektorregister** gespeichert, sofern gerade aktiv.

 -> Verteilung von **Rollen** mit mehr oder weniger eingeschänkten Rechten!

***Auf modernen Computern kommt keine Segmentierung mehr zum Einsatz!***

Ein Überbleibsel ist der **segmentation fault**.