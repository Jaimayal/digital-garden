---
title: "Enhanced Object Literals en JavaScript"
date: "2022-09-28 09:39"
tags: 
  - javascript
draft: false
---
Es una mejora implementada en ES6 a las declaraciones de objetos literales.

## Bindear un Objeto dentro de Otro
En caso de querer agregar un objeto externo a otro objeto, la sintaxis clasica seria la siguiente
```Javascript
	// obj
	obj2: obj2,
	// ...
```

Con la nueva sintaxis, podemos hacer lo mismo de forma mas simplificada

```Javascript
	// obj
	obj2,
	// ...
```

Y listo!

## Escritura de metodos
Antes para agregar un metodo a un objeto teniamos que escribirlo como una propiedad

```JavaScript
const obj = {
	metodo1: function() {
		//,,,
	}
}
```

Pues con la nueva sintaxis ya no, ahora solo es necesario colocar el nombre, sin la keyword function y sin los dos puntos.

```JavaScript
const obj = {
	metodo1() {
		//...
	}
}
```

## Computar nombres
Ademas ahora no necesitamos poner explicitamente el nombre de las propiedades, estas pueden ser computadas por expresiones!

```JavaScript
const obj = {
	[expresion]: valor,
	[`day-${23+3}`]: valor,
}
```