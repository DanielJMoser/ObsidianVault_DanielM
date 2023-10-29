
-> basiert auf dem Prinzip von [[Teile-und-Herrsche-Prinzip|Divide-and-Conquer]]!

## Funktionsweise

Ein **rekursiver Algorithmus**, welcher ein zu sortierendes Array wieder und wieder in **zwei Hälften** teilt, bis eine weitere Teilung **nicht möglich** ist. Dies tritt in zwei Fällen ein:
* Array ist **leer** *(gerade Anzahl an Ausgangselementen)* oder
*  verfügt nur mehr über **ein einziges** Element *(ungerade Anzahl an Ausgangselementen)*

Nach jedem Durchgang wird der neue **Mittelpunkt** eben dieser neu entstandenen Arrays berechnet. **"Left"** (das Element links vom Mittelpunkt) und **"Right"** (Gegenstück) wird verglichen: Ist _Left_ < _Right_? Ansonsten: Tausch!

Dann kann das ursprüngliche Array, nun sortiert, wieder von **unten nach oben** zusammengebaut werden.

------------------

## Anwendung

### Vergleich: Quick Sort

***Bei Quick Sort:*** **Viel Overhead** bei Anwendung mit *Linked Lists*, da diese keinen **Random Access** gestatten![^1] 

***Bei Merge Sort***: **Kleiner Overhead***, da **Random Access** nicht oft notwendig, es wird **sequenziell** vorgegangen.


[^1] Im Gegensatz zu etwa Arrays, welche Elemente **"benachbart"** im Memory Stack ablegen, sind Linked Lists **keine** "in sich abgeschlossenen Speicherblöcke". Man müsste vom Kopf bis zum gesuchten Element _i_ durchiterieren um ein Element zu finden...)


------------------

```python

# Python program for implementation of MergeSort
def mergeSort(arr):
	if len(arr) > 1:

		# Finding the mid of the array
		mid = len(arr)//2

		# Dividing the array elements
		L = arr[:mid]

		# into 2 halves
		R = arr[mid:]

		# Sorting the first half
		mergeSort(L)

		# Sorting the second half
		mergeSort(R)

		i = j = k = 0

		# Copy data to temp arrays L[] and R[]
		while i < len(L) and j < len(R):
			if L[i] < R[j]:
				arr[k] = L[i]
				i += 1
			else:
				arr[k] = R[j]
				j += 1
			k += 1

		# Checking if any element was left
		while i < len(L):
			arr[k] = L[i]
			i += 1
			k += 1

		while j < len(R):
			arr[k] = R[j]
			j += 1
			k += 1

# Code to print the list


def printList(arr):
	for i in range(len(arr)):
		print(arr[i], end=" ")
	print()


# Driver Code
if __name__ == '__main__':
	arr = [12, 11, 13, 5, 6, 7]
	print("Given array is", end="\n")
	printList(arr)
	mergeSort(arr)
	print("Sorted array is: ", end="\n")
	printList(arr)


```

