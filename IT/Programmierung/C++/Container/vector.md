# vector

### std::vector

Inkludiert via **#include < vector >

```cpp

[[include]] vector

std::vector<int> vec; // Erzeugt Container

vec.push_back(42); //Fuegt neues Element am Ende hinzu

int a = vec[0]; //Greift auf Element an der Stelle 0 zu

vec[0] = 123; // Tauscht Element an der Stelle 0 aus

vec.erase(vec.begin()+i); // Loescht Element an der Stelle 0

vec.size(); // Gibt aktuelle Groesse zurueck

vec.clear(); //Entfernt alle Elemente


