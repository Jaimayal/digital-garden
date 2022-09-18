---
title: "Arrays en JavaScript"
date: "2022-09-18 15:24"
tags: 
  - javascript
  - programming
draft: true
---
Los Arrays son una de las estructuras de datos mas basicas de los lenguajes de programacion, y en JavaScript se encuentran implementados de forma dinamica.

Un Array dinamico puede cambiar de tamaño, agregar elementos, quitar elementos y cambiar el contenido (Similar a un ArrayList en Java).

Existen dos formas de crear un Array:
- Sintaxis simple
- Mediante un objeto

La sintaxis simple utiliza un **acortador con corchetes** y los elementos que la conforman:

```JavaScript
const array = ['elem1', 'elem2', 'elem3'];
```

Tambien se puede hacer **instanciando un objeto** de la clase *Array*:

```javaScript
const array = new Array('elem1', 'elem2', 'elem3');
```

Para **acceder a sus elementos** se hace de la misma forma que en lenguajes como C y Java, se utiliza la notacion con \[\] e inicia desde 0:
```JavaScript
console.log(array[0]); // elem1
console.log(array[1]); // elem2
console.log(array[2]); // elem3
```