---
title: "Hash Table"
date: "2022-11-23 09:10"
tags: 
  - 
draft: true
---
Es una estructura de datos que sirve para ordenar elementos con combinacion de diferentes estructuras de datos, usualmente, es una combinacion entre un array y diferentes tipos de listas.

Tambien es referida como un array asociativo, un mapa, un diccionario. La cosa son tener pares de clave-valor.

## Hash Functions
Para lograr tener pares de clave valor tenemos que programar una forma de que a cada llave se le asigne un espacio en memoria. Una hash function se encarga de hacer esto.

Sus caracteristicas principales son
- Consistencia. La misma llave deberia producir siempre el mismo valor.
- Diferencia. Diferentes llaves deben tener diferentes valores y debe evitar repetirse lo maximo posible
- Evita Colisiones. Evita que dos elementos den el mismo valor como resultado y en caso de darlos, sabe como lidiar con ellos usando tora estructura de datos (usualmente una linkedlist).

De esta forma, para acceder a un valor solo debemos darle un valor de una llave, que al pasar a traves del hash function nos dara el resultado que esta guardado ahi.