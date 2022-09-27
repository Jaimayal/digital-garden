---
title: "Short Circuiting en JavaScript"
date: "2022-09-27 15:26"
tags: 
  - javascript
draft: true
---
En JavaScript los operadores logicos AND y OR (&& e ||) sirven para hacer mas que comparaciones logicas.

JavaScript posee un mecanismo que le permite utilizar cualquier valor mas alla de boleanos en ambos lados de la evaluacion logica. Este mecanismo es conocido como short-circuiting.

Esto lo hace utilizando las reglas de los truthy y falsy values.

## OR Short Circuiting
Este mecanismo consiste en que la expresion logica devolvera **el primer termino que sea truthy** y en caso de encontrar falsy values seguira buscando hasta encontrar uno.

```JavaScript
console.log(3 || 'Jaime') // 3 debido a que es un truthy value
console.log('' || 'Jonas') // Jonas debido a que '' es un falsy value y no es devuelto
console.log(true || 0) // true debido a que es un truthy value
console.log(undefined || null); // Aunque los dos sean falsy values el ultimo es devuelto
```

Esto es util debido a que nos podria dar un valor por defecto para una variable

```JavaScript
console.log(obj.number || -1); // imprime obj.number o -1 si no existe
```

## AND Short Circuiting
Este mecanismo es exactamente igual al OR Short Circuiting, solo que esta vez, devolvera **el primer termino que sea falsy** y en caso de encontrar falsy values seguira buscando hasta encontrar uno.

```JavaScript
console.log(0 || 'Jaime') // 0 debido a que es falsy
console.log('Jaime' || '') // '' debido a que es falsy
console.log('jaime' || 23) // 23 debido a que no hay ningun valor falsy
console.log(0 || '') // 0 debido a que es el primery falsy
```