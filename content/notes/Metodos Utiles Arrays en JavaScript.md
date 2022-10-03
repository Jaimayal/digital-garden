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
- includes. Retorna un booleano, true si incluye un elemento, false si no. **Checa por equalidad, solo devuelve true si existe equialidad entre el valor pasado y otro**

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

## forEach()
Se le pasa un callback function como parametro, esta funcion sera llamada por cada iteracion (es decir, por cada elemento).

Como caracteristicas especiales esque a esta callback function le puede pasar hasta un maximo de tres cosas.
1. El elemento actual de la iteracion
2. El indice del elemento actual
3. El array entero

Este metodo en particular tambien funciona con los [[notes/Sets en JavaScript]] y los [[notes/Maps en JavaScript]].

Esta funcion por lo general busca mutar las estructuras de datos de cierta forma!
## Transformaciones de Datos
Existen multiples metodos para transformar los datos de un array.
- map. Aplica una determinada operacion a cada elemento de un array. Devuelve un array nuevo con la operacion aplicada
- filter. Filtra los elementos basado en cierto criterio, solo pasan los que satisfascan la condicion.
- reduce. Reduce todos los elementos a uno solo aplicando una operacion de cada elemento hacia un acumulador. En cada iteracion por cada elemento se debe de devolver el valor del acumulador actualizado con la operacion ya ejecutada

- find. Sirve para encontrar un solo elemento basado en una condicion (o un callback function). Retorna el primer elemento para el cual se obtiene true en la condicion.
- findIndex. Funciona de la misma forma que el metodo find pero devuelve el indice en lugar del elemento
- some. Hace lo mismo que includes pero puede recibir una condicion mas compleja (o un callback function). Por ejemplo si existe un elemento mayor que 0
- every. Hace lo mismo que some pero solo devolvera true si todos los elementos pasan la condicion.

- flat. Sirve para aplanar una estructura de datos que tiene otras anidadas. Devuelve un nuevo array con todos los elementos aplanados. **Como argumento podemos pasarle la cantidad de niveles a aplanar**.
- flatMap. Combina los metodos flat y map en una misma operacion. Primero recibe una operacion para hacer map y al final aplana el resultado. **Este solo funciona con un nivel de nest**.

- sort, Muta el array y lo ordena **basado en strings. primero lo convierte despues hace sorting, es decir, ordena de acuerdo al ascii**. Para arreglarlo se le debe pasa runa **funcion de comparacion como argumento** en forma de callback function. 

Este callback function de comparacion tiene dos argumentos 'a' y 'b'. Se espera un valor positivo o negativo. Si es negativo se colocara 'a' antes que 'b' y si es positivo viceversa.

Crear arrays
- Creacion por brackets []
- Creacion por constructor 
- Creacion por constructor de elementos vacios + Fill
- Creacion por relleno del metodo Array.from. Este recibe un objeto como primer parametro y un callback functionc omo segundo (la cual funciona como un map). Sirve para convertir otra estructura de datos en un array (pasandola como primer parametro).


![[files/MetodosUtilesArraysFramework.png]]