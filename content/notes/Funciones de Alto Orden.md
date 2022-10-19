---
title: "Funciones de Alto Orden"
date: "2022-09-29 12:25"
tags: 
  - programming
draft: false
---
Una funcion de alto orden es toda aquella que recibe como parametro otra funcion, que retorna una funcion o ambas,

Como es logico, son un tipo de funciones generadas gracias a la existencia de las [[notes/Funciones de Primera Clase]].

## Funcion que Recibe otra como Parametro
```JavaScript
const oneWordToLower(str) {
	const [first, ...others] = str.split(' ');
	first = first.toLowerCase();
	return [first, ...others].join(' ');
}

const oneWordToUpper(str) {
	const [first, ...others] = str.split(' ');
	first = first.toUpperCase();
	return [first, ...others].join(' ');
}

// recibe un string y una callback function para ejecutar la transformacion! 
const transformer(str, fn) {
	const finalStrTransformed = fn(str);
}

transformer('Hola me llamo Jaime', oneWordToLower);
```

Otro ejemplo en JS seria la funcion .addEventListener para la [[notes/Manipulacion del DOM]]

```JavaScript
const simple = function() {
	console.log('hi!');
}

// Callback function recibida llamada simple!
document.querySelector('button').addEventListener('click', simple)
```

**La sintaxis de un callback function es escribir su nombre como parametro pero sin parentesis para que sea pasada y despues llamada dentro de la funcion original**.

## Funcion que retorna otra
```JavaScript
const greet = function(greeting) {
	return function (name) {
		console.log(`$[greeting} ${name}`)
	}
}

greet('Hola')('Jaime');
```

Estos mecanismo es especialmente importante para la programacion funcional, debido a que permite encadenar funciones una tras otra

Esto tambien se puede hacer con arrow functions

```JavaScript
const greet = (greeting) => (name) => console.log(`${greeting} ${name}`);

greet('Hola')('Jaime');
```

