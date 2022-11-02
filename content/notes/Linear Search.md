---
title: "Linear Search"
date: "2022-11-02 12:09"
tags: 
  - algorithms
draft: true
---
Es la implementacion mas sencilla de busqueda que existe. Consiste en recorrer de forma lineal elemento por elemento desde el inicio hasta el fin de una estructura de datos comparando si el elemento que buscamos se encuentra en esa posicion o no. Si se llega al final y no hay una coincidencia significa que no existe, por otro lado, si existe, en algun punto se sabra.

Debido a la busqueda lineal, el [[notes/Big O]] de este algoritmo seria **O(n)**.
## Implementacion en Python
```Python
def linear_search(v, arr):
	for a in arr:
		if a == v:
			return True
	return False
```