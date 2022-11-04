---
title: "Queue"
date: "2022-11-02 19:18"
tags: 
  - datastructures
draft: true
---
Es una estructura de datos fundamental basada en FIFO (First in, First Out). Es decir, el primero que este en ella es el primero que va a salir, tal como una cola en la vida real.

Para Insertar un Elemento se requiere que entre al final de la cola. A esta operacion se le llama Enqueue.

Para obtener un Elemento se tiene que remover el primero que se encuentra en la cola. A esta operacion se le llama Dequeue

Lo unico que hace es limitar el numero de operaciones disponibles de una estructura de datos. Muchas veces esta es soportada por nodos debido a que estos tienen un acceso instantaneo a el ultimo y el primer elemento.

Cualquier Queue tiene que cumplir minimo con la siguiente interfaz:
```Java
interface Queue<T> {
	T deque();
	void queue(T o);
	T peek();
}
```

Una codificacion valida seria

```
```