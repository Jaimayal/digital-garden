---
title: "Metodos Utiles Arrays en JavaScript"
date: "2022-09-18 15:29"
tags: 
  - javascript
draft: false
---
Algunos de los metodos mas basicos para trabajar con [Arrays en JavaScript](notes/Arrays%20en%20JavaScript.md):
- push. Apende un elemento al final del array
- unshift. Apende un elemento al **inicio** del array.
- pop. Remuve un elemento al **final** del array
- shift. Remueve un elemento al **inicio** del array
- indexOf. Retorna el indice de un elemento o -1 si no existe
- includes. Retorna un booleano, true si incluye un elemento, false si no.

```JavaScript
const array = ['elem1', 'elem23', 'elem98']

array.push('elem3') // ['elem1', 'elem23', 'elem98', 'elem3']
array.unshift('elem0') // ['elem0', 'elem1', 'elem23', 'elem98', 'elem3']
array.shift() // ['elem1', 'elem23', 'elem98', 'elem3']
array.pop() // ['elem1', 'elem23', 'elem98']

array.includes('elem0') // false
array.indexOf('elem23') // 1
```

- slice Permite extraer un array desde el indice especificado (inclusivo) hasta el otro indice especificado (exclusivo), en caso de no especificar el segundo se hace hasta el final. Esto **no muta el array**. Ademas tambien sirve para hacer un [[notes/Shallow Copy]]!
- splice. Funciona de forma similar al slice pero este **si muta el array, es decir, sus elementos seran diferentes despues de ejecutarlo**.
- reverse. **Muta el array revertiendo el orden de los elementos**
- concat. Concatena dos arrays y devuelve uno nuevo.
- join. Une todos los elementos en uno solo utilizando el delimitador especificado como parametro. 

## at()
Es una forma de reemplazar la notacion tradicional de los corchetes para acceder a los elementos del array.

Lo que lo diferencia esque se pueden utilizar indices negativos y positivos para obtener elementos como en los metodos slice y splice.

```JavaScript
console.log(array[array-1]); // same
console.log(array.at(-1)); // same
```

