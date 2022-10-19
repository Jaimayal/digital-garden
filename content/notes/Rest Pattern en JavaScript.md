---
title: "Rest Pattern en JavaScript"
date: "2022-09-27 12:13"
tags: 
  - javascript
draft: false
---
Utiliza la misma sintaxis del [[notes/Spread Operator en JavaScript]], sin embargo, hace lo contrario, recolecta multiples elementos y los condensa en una sola estructura, un array.

**Notemos que se utuliza donde pondriamos variables separadas por comas**.

En este caso, para reconocerla, podemos ver que los tres puntos '...' se encuentran del **lado izquierdo de la asignacion**.

Para utilizarla, podemos combinarla de forma simple con el [[notes/Destructuring en JavaScript]].

```JavaScript
const array = [1, 2, 3];
const [valor, ...otrosValores] = array; // valor = 1, otrosValores = [2, 3]
```

Se utiliza el sobrenombre rest pattern debido a que **recolecta el resto de elementos de una estructura de datos**.

## Caracteristicas
- Solo puede existir un rest pattern en una asignacion
- Debe ser el ultimo elemento del destructuring.

## Aplicado a Funciones
Ppodemos aplicarlo a los parametros, al aplicarlo se les llama **rest parameters** y de esta forma podemos pasarle una cantidad indefinida de parametros a una funcion.

```JavaScript
const sum = function(...numbers) {
	let sum = 0;
	numbers.forEach(number => sum += number);
	console.log(sum);
}
```