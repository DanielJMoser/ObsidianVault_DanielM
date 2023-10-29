# Binärer Suchbaum
-> **gerichteter Graph**, entweder **leer** oder mit **genau zwei** Verstrebungen zu Unterbäumen.

## Terminologie

#### Blätter
-> Knoten, deren Äste **null** sind (Sackgassen)

#### Root
-> Oberste Wurzel des Baumes

#### Höhe
-> Anzahl der Knoten des Baumes

-----------------

**Beispiel:
```mermaid 
graph TD; 
id1((2)) --> id2((7));
id1((2)) --> id3((5));
id2((7)) --> id4((2));
id2((7)) --> id6((6));
id3((5)) --> id7((9));
id3((5)) --> id8((4));
id6((6)) --> id9((5));
id6((6)) --> id10((11)); 
```



