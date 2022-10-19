---
title: "Metodo apply en JavaScript"
date: "2022-09-30 08:22"
tags: 
  - javascript
draft: false
---
Es otro metodo que puede ser aplicado en las funciones que nos sirve para cambiar a donde apunta la keyword [[notes/this en JavaScript]].

Tiene exactamente la misma funcionalidad que [[notes/Metodo call en JavaScript]], sin embargo, este metodo **no permite recibir los argumentos de la funcion separados por comas, recibe un array de argumentos**.

```JavaScript
funcion.apply(thisKeywordReplacer, [args]) // El primer argumento sera el objeto o cosa que sustituira la keyword this y el segundo los argumentos de la funcion normal
```

Reutilizando el ejemplo 

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

funcion.call(obj1, [2]); // Jaime: 20
funcion.call(obj2, [23]); // Pepe: 5
```

**Este metodo ya no es tan utilizado gracias a la existencia de [[notes/Metodo call en JavaScript]] y el uso del [[notes/Spread Operator en JavaScript]] en caso de ser necesario**.