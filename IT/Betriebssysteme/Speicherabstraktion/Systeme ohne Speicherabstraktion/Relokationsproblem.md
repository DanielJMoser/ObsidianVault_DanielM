## Relokationsproblem

-> ***Bei Multitasking-Systemen***

Mehr als ein Programm im Speicher -> Problematisch!

* Programme müssen an **mehr als einer** Stelle in den Speicher geladen werden.
* Sprungadresse stimmt u.U. nicht mehr.
* Globale Variablen ev. an falscher Stelle.
* z.B. springt "jmp 28" nun an die falsche Stelle.

Zum Zeitpunkt des **Kompilierens** bzw. des **Linkens** ist nicht bekannt, an welcher Stelle das Programm geladen wird.

-> ***Relokationsproblem***

_____

### Mögliche Lösungen

#### Statische Relokation

Beim Laden wird Speicheradresse umgeschrieben. Lade-Offset wird addiert. So würde aus **"jmp 28"** z.B. **"jmp 16412"** werden.


#### Dynamische Relokation

Verwendung von [[Segmentierung]]!

* Jedem Prozess wird ein exklusives Segment zugewiesen.
* Speicheradressen werden als Segment-Offset interpretiert
* So würde beim Ausführen von **"jmp 28"** automatische die **"Segment-Basisadresse"** hinzuaddiert werden.



