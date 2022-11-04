---
title: "ArrayList"
date: "2022-11-04 09:57"
tags: 
  - datastructures
draft: true
---
Combina lo mejor del mundo del [[notes/Array]] y del [[notes/Linked List]].
- Acceso a un elemento con O(1)
- Puede crecer y cambiar de tamaño

Esto es posible debido a que:
1. Se utiliza un Array en lugar de Nodos para soportar la lista
2. Se lleva un control de la longitud para saber si al insertar un elemento todavia cabe basado en la capacidad maxima.
3. En caso de exceder la capacidad maxima, se copia todo el contenido del array a un array con mayor capacidad.
4. Las operaciones de una [[notes/Queue]] aplicadas aqui son muy ineficientes.
	1. La operacion Enqueue() requiere [[Big o]] de O(n) debido a que, si se inserta al inicio de la lista donde ya hay un dato se tendran que mover todos los demas datos una unidad y sera muy ineficiente.
	2. La operacion Dequeue() tambien requiere de O(n) debido a que cuando se remueve un elemento todos los demas tienen que avanzar. Escencialmente tendriamos que hacer la correccion de mover todos los elementos una unidad hacia atras para que en la primera posicion (0) exista algo.
5. Las inserciones a la mitad de la lista tambien tienen que mover toda la lista a la derecha suya. 
