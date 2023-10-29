# Template Specialization

### (Siehe: [[_Templates]])
Für eine bestimmte Parameterausprägung wird eine spezielle Implementierung ausgegeben.
Ist etwa für den angegebenen Datentypen einer *sum*-Funktion der **"+=" Operator** nicht definiert, so würde es ohne der Specialization zum Compilierfehler kommen.

```cpp

template <>
MySpecialClass sum (MySpecialClass array[], int n) {
	MySpecialClass result;
	for ( int i = 0; i < n; i++);
		result = result .add(array[i]);
		}
	}
	return result;
}

// Kein Compilierfehler mehr!

MySpecialClass array[10];
MySpecialClass result = sum<MySpecialClass> (array, 10);
```

