---
title: "Sets en JavaScript"
date: "2022-09-28 12:20"
tags: 
  - javascript
draft: true
---
Un set es una estructura de datos que no permite ningun elemento repetido. En JavaScript fue introducido en ES6 junto con los Maps en JavaScript.

Para crear un nuevo set utilizamos la instanciacion de un objeto y como parametro le podemos pasar un objeto que sea Iterable (Como un array o un String).

```JavaScript
const set= new Set(array);
```

- En caso de tener elementos duplicados, el Set se encargara de eliminarlos a todos ellos. 
- Es una estructura desordenada, por tanto, no le importan el orden de los elementos y nunca esta garantizado que los de en determinado orden.
- No hay forma de obtener valores desde un Set.
- Son **iterables**

**Son mayormente utilizados para filtrar los elementos de un array y quedarse con los valores unicos**. Combinandolo con el [[notes/Spread Operator en JavaScript]] que funciona sobre todos los iterables podemos obtener un array de vuelta!

```JavaScript
const array = [1, 2, 3, 3, 1, 4, 1];
const uniques = [...new Set(array)];
```

## Metodos Utiles
```JavaScript
set.size // Devuelve el tamano de la estructura
set.has(elem) // Devuelve un booleano es como includes de los arrays
set.add(elem) // agrega un elemento al array
set.remove(elem) // remueve un elemento del array
```

