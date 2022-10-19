---
title: "For of Loop en JavaScript"
date: "2022-09-28 08:59"
tags: 
  - javascript
draft: false
---
Es un nuevo tipo de for que fue agregado en ES6 como otra forma de iterar sobre estructuras de datos con una sintaxis mas simple sin preocuparte por contadores o condiciones.

Este loop simplemente iterara sobre la estructura elemento por elemento. (Es bastante similar al foreach loop de Java).

```JavaScript
for (const element of elements) {
	console.log(element); // Para cada elemento de elemenetos imprimelo
}
```

Este loop estaba concebido para no brindar el indice de los elementos, sin embargo, existe una forma de obtenerlos

```JavaScript
for (const entry of elements.entries()) {
	console.log(entry);
}
```

La funcion .entries() es un array de arrays en el que cada uno contiene el indice y su elemento particular.

En este caso, cada entry sera un array que contiene el indice y su elemento.

![[files/ForOfConEntriesJS.png]]

Y ahora podemos utilizar la poscion 0 para referirse al indice y la posicion 1 para referirse al elemento.

O mejor aun... podriamos utilizar el mecanismo de [[notes/Destructuring en JavaScript]] para darle al indice y al elemento un nombre!

```JavaScript
for(const [index, element] of elements.entries()) {
	console.log(`${index}: ${element}`);
}
```