
-> Simpelster Algorithmus, welcher auf Basis **wiederholtem Plätzetauschens** basiert.

Da seine [[Laufzeitkomplexität]] recht hoch ist, eignet er sich nicht besonders gut für größere Datensätze.

-----------------------


```python

# Python program for implementation of Bubble Sort


def bubbleSort(arr):
	n = len(arr)

	# Durch alle Elemente iterieren
	for i in range(n):

		# Die letzten i Elemente sind bereits an der richtigen Stelle
		for j in range(0, n-i-1):

			# Iteriere durch das array von 0 bis n-i-1
			# Swap if the element found is greater
			# than the next element
			if arr[j] > arr[j+1]:
				arr[j], arr[j+1] = arr[j+1], arr[j]


# Driver code
arr = [64, 34, 25, 12, 22, 11, 90]

bubbleSort(arr)

print("Sorted array is:")
for i in range(len(arr)):
	print("%d" % arr[i], end=" ")

```