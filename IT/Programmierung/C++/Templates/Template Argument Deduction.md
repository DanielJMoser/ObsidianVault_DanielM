# Template Argument Deduction

Siehe: [[_Templates]]

Aus z.B. Eingabeparametern versucht der Compiler, automatisch konkrete **Parameterwerte** abzuleiten. So können die spitzen Klammern oftmals weggelassen werden:

```cpp

int array1[10];
int result1 = sum(array1, 10);
//
//
float array2[10];
float result2 = sum (array2, 10);
```

