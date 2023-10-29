# Iteratoren

Werden für den Zugriff auf **Daten** (in z.B. Listen, Arrays, Containern,...) verwendet! -> Schleifen!
Im Bereich der ==Datenbanken== wird dieser auch **Cursor** genannt.


### Bei [[Daten-Container|Containern]] in C++

Iteratoren sind **abstrakte Objekte**, die eine **einheitliche Schnittstelle** bieten.

- Einheitlicher Zugriff auf Inhalt verschiedener Container-Implementierungen
- Kapselung von Implementationsdetails der Container

Sie iterieren über die einzelnen Elemente eines Containers, meist allerdings nur **entweder vor- oder rückwärts**.


Alle [[Daten-Container|Container]] der Standardbibliothek besitzen zwei Objektfunktionen, die Iteratoren zurückgeben:

- ==*begin() bzw. rbegin()*== -> zeigt auf das erste bzw. letzte Element.
- ==*end bzw. rend()* ==-> zeigt auf das letzte bzw. erste Element.


Um den Iterator weiterzubewegen, wird der Inkrementoperator "**++**" verwendet (z.B. "i++").

Eine **For-Schleife** eines [[vector]] würde so aussehen:

```cpp

[[include]] <vector>
std::vector vec1;
for (std::vector<int>::iterator it = vec1.begin();
	it != vec1.end(); it++) {
		std::cout << *it << std::endl;
}
```