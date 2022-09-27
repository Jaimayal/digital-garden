---
title: "Destructuring en JavaScript"
date: "2022-09-27 08:31"
tags: 
  - javascript
draft: true
---
Es un mecanismo de [[notes/JavaScript]] que sirve para desestructurar una estructura de datos hacia multiples variables.

Para esto, existe una sintaxis especial que sirve para declarar multiples variables basada en los elementos que ya tiene una estructura de datos.

Veamos un ejemplo 
```JavaScript
// Array inicial
const array = [1, 2, 3];

// Destructuracion
const [x, y, z] = array; // Asignacion de desestructura
console.log(x) // 1
console.log(y) // 2
console.log(z) // 3
```

**Esta forma de deconstruccion duplica los elementos de un array, por tanto, si son modificados no afetara al array original.**

Adicionalmente, el destructuring tambien es util para intercambiar dos valores de variables.

```JavaScript
let [main, sec] = {1, 2}; // [1, 2];
[main, sec] = [sec, main]; // [2, 1];
```