---
title: "Linked List"
date: "2022-11-02 18:55"
tags: 
  - datastructures
draft: true
---

En comparacion con un [[notes/Array]] este si permite eliminar e insertar elementos (mas alla de solo sobreescribirlos). Ademas puede crecer de tamaño y reducirlo como le apetezca.

Su unidad mas basica es un nodo el cual guarda referencia al siguiente nodo y un valor.

## Singly Linked List

## Doubly Linked List

Es lo mismo que una lista, sin embargo, en esta cada nodo no solo guarda una referencia para el siguiente nodo si no una para el nodo anterior a ella. 

```C
typedef struct node {
	int val;
	struct node *next;
} node
```

En un lenguaje moderno se podria implementar con genericos (parametrizacion) de forma mas facil y general.

## Insercion y Delecion
Cualquier insercion y delecion solo requiere un cambio en los valores de los nodos que se conectan.

Por tanto, sin importar los elementos de la operacion o la cantidad de nodos que tenga la estructura, la insercion y delecion tiene un [[notes/Big O]] de O(1).

Lo que cuesta es viajar hasta el elemento que se desea eliminar, o en la posicion a la que se desea agregar. Estos tienen un O(n).

