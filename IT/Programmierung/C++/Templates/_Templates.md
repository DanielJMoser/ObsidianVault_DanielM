# Templates

### Vergleich: Python
In **Python** würde eine *sum*-Funktion etwa so aussehen:

```python
def sum(array):
	result = 0
	for e in array: 
		result += e
	return result
```

[[Datentypen]] (float oder int?) werden hier nicht angegeben, da diese vom Compiler selbstständig beachtet werden.

### In C++:


In **C++** siehe selbiger Code anders aus. Hier müssten zwei Funktionen geschrieben werden:

```cpp

int sum (int array[], int n) {
	int result = 0;
	for (int i = 0; i < n; i++) {
		result += array[i];
		}
	}
	return result;
}

int float (float array[], int n) {
	float result = 0;
	for (int i = 0; i < n; i++) {
		result += array[i];
		}
	}
	return result;
}
```

^b78a07


Diese sind bis auf die Datentypen Ident! Ein [[Metaprogramm]] kann hier helfen, unnötigen Code zu vermeiden und die Datentypen auszutauschen:

```cpp
//Function Prototype
template <typename T>
T sum (T array[], int n);

//Function Implementation
template <typename T>
T sum (T array[], int n) {
	T result = 0;
	for (int i = 0; i < n; i++) {
		result += array[i];
	}
	return result;
}
```

Statt *int* und *float* wird der Parameter *T* verwendet. Implementierung wie folgt:

```cpp
int array1[10];
int result1 = sum <int>(array1, 10);

float array2[10];
float result2 = sum<float>(array2, 10);

class MyClass {...};
MyClass operator += (const MyClass& a, const MyClass& b) {...}

MyClass array3[10]
MyClass result3 = sum<MyClass> (array3, 10); 
```


Wir unterscheiden zwischen folgenden Arten von Templates:

- [[Function Templates]]
- [[Class Templates]]
- Variable Templates
- Alias Templates


Oftmals können die spitzen Klammern auch weggelassen werden: [[Template Argument Deduction]]

Code-Generierung funktioniert **on-demand**, stößt der Compiler also auf ein Template, wird dieses erst relevant, wenn explizit aufgerufen. Da jede cpp-Datei eine eigenständige **Compilation Unit** bildet, also unabhängig voneinander übersetzt wird, können Templates ebenfalls nicht einfach vorkompiliert und in mehreren Files eingesetzt werden. ( [[on-demand]] )

***Zum Einsatz in mehreren Compilation Units*** -> Alle Bestandteile des Templates ins jeweilige **Header-File!**


Obige *sum*-Funktion kann nur für Datentypen eingesetzt werden, für die der **"+="-Operator** definiert ist. Um das zu umgehen: [[Template Specialization]].

### Probleme mit Templates

- **_Nicht einfach zu verwenden! 
Fortgeschrittene Features brauchen viel Hintergrundwissen!
  - Code wird unübersichtlich
  - Komplexe Templates schwer zu durchschauen

- **_Nichtssagende Fehlermeldungen
  - Fehlermeldungen oft nur Folgefehler, daher schwer zu debuggen
  - **Concepts** sollen das (ab C++20) ändern.
  
- **_Speicher- und Rechenintensiv bem Kompilieren und Analysieren
  - Statische Codeanalyse in IDEs wird dadurch erschwert.

- **_Keine Saubere Trennung von Deklaration und Definition 
  - Siehe: oben ( [[on-demand]] )


