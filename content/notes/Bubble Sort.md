---
title: "Bubble Sort"
date: "2022-11-02 18:20"
tags: 
  - algorithms
draft: true
---
Es un Algoritmo de Ordenamiento que sirve para ordenar una estructura de datos.

En cada iteracion el elemento mas grande "flotara" hasta la ultima parte del array, es decir, en cada iteracion se reduce el numero de elementos  a ordenar en uno porque el ultimo siempre estara ordenado.

Este algoritmo cuenta con [[notes/Big O]] de O(n^2).

## Implementacion en Python
```Python
def bubble_sort(arr):
	for i in len(arr):
		for j in range(0, len(arr) - i):
			if arr[i] > arr[j]:
				temp = i
				i = j
				j = temp
```