---
title: "Maps en JavaScript"
date: "2022-09-28 15:21"
tags: 
  - javascript
draft: false
---

La diferencia entre objetos y mapas esque en los mapas las keys pueden ser de cualquier tipo de dato (No como en los objetos, que solo permiten strings).

Para utilizarlos, tambien utilizamos la sintaxis del constructor

```JavaScript
const map = new Map();
```

## Agregar Elementos
Una vez creado el mapa, podemos empezar a agregar elementos con el metodo set.

```JavaScript
map.set('key', 'value');
map.set(2, true);
map.set(false, 'somevalue');
```

El metodo set returna el mapa ya modificado (mutado), esto nos permite encadenar multiples set consecutivos

```JavaSCRIPT
map.set('key2', 'value2')
	.set(true, 'Esta abierto')
```

## Obtener Elementos
Para obtener un elemento debemos referirnos a el mediante su key y se nos devolvera su valor con el metodo get

```JavaScript
map.get('key');
map.get(2);
map.get(false);
```

## Checar si Existe
Para checar si un elemento existe volvemos a reutilizar el metodo .has

```JavaScript
map.has('key');
```

## Eliminar Elementos
Para eliminar utilizamos el metodo .delete

```JavaScript
map.delete('key');
```

## Otra alternativa de agregar elementos
Otra forma de declarar un mapa es utilizar un array de arrays.

```JavaScript
const map = new Map([
	['key', 'value']
	['key', 'value']
])
```

Extrañamente familiar a los metodos utilizados en [[notes/Loopear sobre Objetos en JavaScript]] (Object.entries). Debido a esto, es muy sencillo pasar un objeto a un mapa!

```JavaScript
const map = new Map(Object.entries(obj)); // Convierte un objeto a un mapa
```

## Iteracion
Su iteracion es exactamente igual que en [[notes/Loopear sobre Objetos en JavaScript]], se utiliza la [[notes/Destructuring en JavaScript]] para obtener el par de llave - valor.

```JavaScript
for(const [key, value] of map) {
	console.log(`${key}: ${value}`);
}
```

```JavaScript
// challenge
question.get(answer === question.get('correct'));
```