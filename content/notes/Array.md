---
title: "Array"
date: "2022-11-02 09:07"
tags: 
  - datastructures
draft: true
---
Un Array es una estructura de datos de tamaño arreglado que guarda informacion de forma continua en memoria, una detras de la otra. Esto significa que esta estructura no puede crecer.

```Java
int[] arr = new int[3]
```
'arr' es una referencia que apunta al inicio de un array de enteros.

La asignacion serian tres espacios continuos que pueden guardar un entero dentro de ellos.


## Obtener datos en un Indice Especifico
Para obtener datos se tiene que hacer desde un indice especifico. 

Para obtener una posicion exacta dentro de un array primero se debe multiplicar un offset de memoria por la posicion deseada. Gracias a los lenguajes con sistema de tipos el offset es inferido por el tipo de dato y nada mas tenemos que obtener la posicion deseada

```Java
int[] arr = {4, 5, 6}
int val = arr[1]
```

Efectivamente lo que hace este codigo es *Desde el inicio desplazate una unidad de memoria de 32 bits (int) y guardamela en la variable 'val'*. De esta manera, obtenemos el valor 5.

## Manipular datos en un Indice Especifico
Para insertar y eliminar datos dentro de un array no se reduce ni incrementa el tamaño del array, sino directamente sobreescribe los datos que se encuentren en la posicion deseada.

```Java
int[] arr = {3, 4, 5}
arr[1] = 0;
```


## Compromiso
### Ventajas
- Acceso por indice a cualquier valor (Debido a que por aritmetica de pointers podemos acceder a cualquier valor). **Acceso Aleatorio**
- O(1) Todo, traer y guardar informacion.
- Insertar un elemento a una posicion especifica sin afectar al resto requiere de O(n) para mover todos los elementos a otras posiciones.

### Desventajas
- Usa memoria de forma constante, no cambia hasta cuando esta sin usar
- Imposible agregar mas elementos de los requeridos inicialmente 