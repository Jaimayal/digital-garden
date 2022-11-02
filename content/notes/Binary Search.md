---
title: "Binary Search"
date: "2022-11-02 12:21"
tags: 
  - 
draft: true
---
Es uno de los algoritmos mas clasicos y una de las bases para otros algoritmos puesto que es el primer algoritmo que requiere que la estructura de datos este ordenada.

El algoritmo consiste en saltar entre la estructura partiendola en la mitad cada vez hasta

Debido a los saltos entre la estructura, el [[notes/Big O]] de este algoritmo es **O(log n)**.

## Implementacion en Python
```Python
def binary_search(v, arr):
	start = 0
	end = len(arr)

	while start < end:
		mid = start + (end - start) / 2
		val = arr[mid]
		if val == v:
			return True
		elif val > v:
			end = mid
		else:
			start = mid + 1
```

