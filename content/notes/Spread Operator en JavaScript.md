---
title: "Spread Operator"
date: "2022-09-27 11:51"
tags: 
  - javascript
draft: true
---
El Spread Operator es un operador que sirve para aplanar los elementos de un array, funciona como recorrer todo el array y colocarlo en variables independientes utilizando lel [[notes/Destructuring en JavaScript]], sin embargo, nos da una sintaxis super simple y limpia de trabajo.

**Notemos que se utiliza donde se colocarian valores separados por comas.**

Tiene una sintaxis muy similar al [[notes/Rest Pattern en JavaScript]], sin embargo, el operador de los tres puntos '...' se encuentra del **lado derecho de la asignacion**.

```JavaScript
const array = [7, 8, 9];
const newArray = [1, 2, ...array]; // 1, 2, 7, 8, 9

console.log(newArray); // [1, 2, 7, 8, 9]
console.log(...newArray); // 1 2 7 8 9
```
Esta sintaxis como **resultado da todos los valores del array separados por comas**, por tanto, no crea ninguna variable.

**Este operador funciona en todos los objetos que son 'iterables'**. Estos son arrays, strings, mapas, sets y otros.

Sin embargo, apartir de ES6 tambien funciona con objetos.

```JavaScript
const oldObj = {
	nombre: 'Rest'
	direccion: '123'
}

const newObj = {
	...oldObj, // Todo lo de oldObj 
	propied1: 2323, 
	creacion: 1999
}
```

Se utiliza el sobrenombre spread porque **expande (aplana) los elementos del array**.

## Aplicado a Funciones
Podemos aplicar un aplanmiento directo a un array que pasemos a una funcion como parametros

```JavaScript
const sum = function(number1, number2) {
	console.log(number1 + number2);
}

const array = [2, 3];
sum(...array);
```