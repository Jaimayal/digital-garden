---
title: "Logical Assignment Operators en JavaScript"
date: "2022-09-28 08:12"
tags: 
  - javascript
draft: false
---
Son operadores con sintaxis similar a los operadores de acumulacion. En este caso, los operadores logicos de asignacion sirven para comparar [[notes/Propiedades de Objetos en JavaScript]] y aplicar el mecanismo de [[notes/Short Circuiting en JavaScript]] para, por ejemplo, dar un valor por defecto a una propiedad.

## Operador OR
Este operador asigna el valor a la propiedad si su valor actual es falsy.

```JavaScript
obj.propiedad = obj.propiedad || 1; // normal con short circuiting
obj.propiedad ||= 1; // operador de asignacion + short circuiting
```

## Operador Nullish Coalescing
Este operador funciona de la misma forma que el OR pero solo lo asigna si su valor actual es nullish (null o undefined).

```JavaScript
obj.propiedad ??= 1; // operador de asignacion + short circuiting
```

## Operador AND
Adicionalmente tambien existe el operador AND que asigna un valor solo si su propiedad actual es truthy.

```JavaScript
obj.propiedad &&= 23; // Si es truthy obj.propieda asignale el valor 23
```