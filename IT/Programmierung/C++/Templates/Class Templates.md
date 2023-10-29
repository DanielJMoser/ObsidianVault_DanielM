# Class Templates

### Klassen-Template: Sicheres Array

```cpp

template <typename T, int N>

class MyArray {
private:
	T array[N];
public:
	T& operator[](int indx);
};

template <typename T>
T& MyArray <T>::operator[](int idx) {
	if (idx < 0 || idx >= N) {
		throw std::runtime_error("index_out_of_bounds");
	}
	return array[idx];
}
```

So kann ein **sicheres Array** für beliebige Datentypen implementiert werden!

### Verwendung:

```cpp

MyArray array;
array[0] = 42;
int a = array [0];
array [42]= 42; //Wirft Exception

MyArray<float, 10>* array = new MyArray<float, 10> (*array) [0] = 42;
int a = (*array)[0];
(*array)[42] = 42; // Wirft Exception
```

Buffer-Overflows/- Underflows werden somit vermieden.