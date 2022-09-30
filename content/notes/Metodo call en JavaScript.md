---
title: "Metodos call y apply en JavaScript"
date: "2022-09-29 22:10"
tags: 
  - javascript
draft: true
---
Es un metodo muy util que sirve para aplicar una funcion global como si fuese llamada desde un objeto. De esta forma, hacemos que la keyword [[notes/this en JavaScript]] apunte al objeto en cuestion y no a undefined o window.

Su sintaxis basica es:

```JavaScript
funcion.call(thisKeywordReplacer, args) // El primer argumento sera el objeto o cosa que sustituira la keyword this y el segundo los argumentos de la funcion normal
```

Un ejemplo claro seria el siguiente: 

```JavaScript
const obj1 = {
	name: 'Jaime',
	age: '20',
}

const obj2 = {
	name: 'Pepe',
	age: '5',
}

function funcion(day) {
	console.log(`${this.name}: ${this.age} at ${day}`);
}

funcion.call(obj1, 2); // Jaime: 20
funcion.call(obj2, 23); // Pepe: 5
```