# Object Ownership

Wer ist für den **Lebenszyklus** von Objekten zuständig?
Wer erzeugt Objekte?
Wer speichert diese?
Wer zerstört sie und gibt Speicher wieder frei?

Ist die Object Ownership am Heap nicht klar geregelt, so drohen **Memory Leaks**! 
In der Regel übernehmen andere Objekte die Object Ownership. Auf diesem Wege können rekursiv ganze Bäume entstehen. Wird das Mutterobjekt zerstört, so 
auch alle Tochterobjekte.

Besonders [[Smart Pointer]] können hier sehr hilfreich sein! 


