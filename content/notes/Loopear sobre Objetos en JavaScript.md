---
title: "Loopear sobre Objetos en JavaScript"
date: "2022-09-28 10:08"
tags: 
  - javascript
draft: false
---
Aunque los objetos en javascript no tienen la propiedad de ser iterables, existe una forma de obtener un conjunto de elementos que si integran esta propiedad.

Debido a que los objetos no son iterables, tenemos que conseguir una forma de pasarlos a un array. Es ahi donde entra las funciones de Object.

Tambien nos apoyaremos en la sintaxis especial del [[notes/For of Loop en JavaScript]].

Existen tres alternativas dependiendo de lo que busquemos conseguir.

## Keys - Nombre de Propiedades
La funcion especial que utilizamos es Object.keys().

```JavaScript
for(const key of Object.keys(obj)) {
	console.log(key) // cada nombre de propiedad
}
```

## Values - Valores de las Propiedades
La funcion especial que utilizamos es Object.value().

```JavaScript
for(const value of Object.values(obj)) {
	console.log(value) // cada valor de propiedad
}
```


## Entries - Ambos
La funcion especial que utilizamos es Object.entries(). Esta funcion retorna un array en el cual cada elemento es un array conteniendo el key y el value de cada propiedad.

Por tanto, es muy conveniente utilizar [[notes/Destructuring en JavaScript]] para conseguir las dos variables separadas.

```JavaScript
for(const [key, value] of Object.entries(obj)) {
	console.log(`${key}: ${value}`);
}
```

Como se nota es bastante similar a lo que utilizamos en el array del ejemplo de [[notes/For of Loop en JavaScript]].