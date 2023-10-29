
# Verkettete Listen
-> Eine **dynamische Datenstruktur**, deren Elemente **linear** angeordnet sind. Jedes Element besteht aus:

- Key
- den eingentlichen Daten
- Pointer auf das **nächste Element in der Reihe**

So besteht eine liste aus dem Verweis auf das 
**erste Element der Reihe** und damit auf 
**alle so erreichbaren Elemente**.


![[Drawing LinkedList.png]]

Zum Einfügen/Löschen muss nur ein Pointer umgesetzt werden.

---------------------

## Mögliche Operationen
- insertAtStart(e)
- insertAtEnd(e)
- insertSorted(e)
- delete(e)
- **append(Liste) -> Liste am Ende einfügen
- **splice(List, position) -> Liste mittendrin einfügen
- print(Liste)
