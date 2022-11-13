---
title: "Quick Sort"
date: "2022-11-05 15:12"
tags: 
  - algorithms
draft: false
---
Es un Algoritmo de Sorting mucho mas rapido que [[notes/Bubble Sort]] o Selection Sort. Esta basado en [[notes/Divide-and-conquer]].

El caso Base de Quick Sort es el array mas sencilo de ordenar, es decir, un array de longitud 1 o 0.

Otro caso sencillo de ordenar es cuando un array tiene dos elementos, estan facil como cambiarlos de lugar para ordenarlos bien.

En un array de mas de dos elementos, se tiene que elegir un elemento especial llamado **pivot** de entre los que componen el array. Posteriormente, buscar los elementos menores que el pivot y ordenarlos en torno a el. A este proceso se le llama **Partitioning**.

El resultado de una particion es tener:
- Un array de elementos menores que el pivote
- El pivote
- Un array de elementos mayores que el pivote

Y posteriormente aplicamos recursividad a cada uno de los arrays, si es de menos de dos o menos elementos los ordenados, si no, los volvemos a particionar hasta tenerlos ordenados.

Posteriormente el resultado de cada recursion sera el array izquierdo + el pivote + el array derecho, ya todo ordenado

![[files/QuickSort.png]]

## Implementacion en Python
```Python
def qsort(arr):
    length = len(arr)
    if length < 2:
        return arr
    pivotIdx = round(length / 2)
    low = []
    high = []
    for n in range(0, len(arr)):
        if n != pivotIdx:
            if arr[n] > arr[pivotIdx]:
                high.append(arr[n])
            elif arr[n] <= arr[pivotIdx]:
                low.append(arr[n])
    return qsort(low) + [arr[pivotIdx]] + qsort(high)

print(qsort([5, 3, 2, 1, 4, 8, 3, 1, 9]))
```


