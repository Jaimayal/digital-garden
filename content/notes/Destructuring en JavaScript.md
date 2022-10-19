---
title: "Destructuring en JavaScript"
date: "2022-09-27 08:31"
tags: 
  - javascript
draft: false
---
Es un mecanismo de [[notes/JavaScript]] que sirve para desestructurar una estructura de datos hacia multiples variables.

Para esto, existe una sintaxis especial que sirve para declarar multiples variables basada en los elementos que ya tiene una estructura de datos.

### Desestructurando Arrays
Se utiliza la sintaxis con corchetes, el orden de los elementos importa.

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

Y tambien sirve para desestructurar estructuras anidadas
```JavaScript
const nested = [2, 4, [5, 6]]; // array nested
const [i, , [j, k]] = nested; // 2, 5, 6
```

Adicionalmente, tambien podemos conseguir valores por defecto en caso de que estos no se encuentren o se salgan del rango maximo del array
```JavaScript
const array = [1, 2];
const [one = -1, two = -1, three = -1] = array; // 1, 2, -1
```

### Desestructurando Objetos
#### Variables Inmutables
En este aso, se utiliza la sintaxis con llaves, el orden de los elementos no importa mientras tengan el mismo nombre de las propiedades dentro de los objetos.


```JavaScript
const {propiedad1, propiedad2, propiedad3} = objeto;
```

De esta manera, cada variable obtendra su respectiva propiedad y podra trabajar de manera individual.

#### Variables Mutables
En caso de estar trabajando con variables mutables, debemos notar que lo siguiente dara error de sintaxis debido a que JavaScript toma los corchetes como un inicio de bloque de codigo, por tanto, no puede hacer una asignacion.
```JavaScript
let a = 3;
let b = 4;
{a, b} = obj; // SIntaxis incorrecta
```

Para hacer esto, debemos utilizar un parentesis al rededor de toda la expresion.
```JavaScript
let a = 3;
let b = 4;
({a, b} = obj); // Sintaxis valida
```

#### Cambiar Nombres
Adicionalmente, tambien podemos cambiar el nombre de las propiedades a otro que deseemos.

```JavaScript
const {
	propiedad1: nombreDeseado1, 
	propiedad2: nombreDeseado2, 
	propiedad3: nombreDeseado3
} = objeto;
```

#### Valores por Defecto
Tambien podemos asignar un valor por defecto en caso de que la propiedad no exista dentro del objeto. De esta forma evitamos tener 'undefined'.

```JavaScript
const {propiedad1 = valorPorDefeto} // En caso de no ser encontrado, seras vlaorpordefecto
const {propiedad1: nombreDeseado1 = valorPorDefecto} // Lo mismo pero sintaxis combinada
```

#### Mutabilidad del Objeto
En este caso, al utilizar la desestructura se te devuelve la misma referencia a los objetos que estan contenidos dentro del objeto. Por tanto, si cambias tus variables cambiaras las de tu objeto tambien.

```JavaScript
const {name, mainMenu, starterMenu} = restaurant;

console.log(mainMenu);
console.log(restaurant.mainMenu);

mainMenu.push('Pizza23');
console.log(mainMenu);
console.log(restaurant.mainMenu); 
```

#### Objectos Anidados
Existe tambien una sintaxis especial para lidiar con objetos anidados dentro de objetos. Suponiendo que tenemos el siguiente objeto con objetos anidados:

```JavaScript
const restaurant = {
  name: 'Classico Italiano',
  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  },
};
```

La forma de obtener, por ejemplo, las horas del dia sabado seria utilizando la sintaxis de cambio de nombres + una anidacion:

```JavaScript
const {openingHours: {sat: {open, close}}} = resturant;
console.log(open, close) // 0, 24
```

#### Aplicacion a Funciones
En JavaScript usualmente las funciones suelen tener muchos argumentos, una forma de lidiar con ellos es utilizar un objeto para enviar los parametros, dentro del objeto que recibe la funcion, podemos hacer desestructuracion directamente!.

```JavaScript
const obj = {
	attrib: 1

	func: function({parametro1 = 1, parametro2 = 1}) {
		console.log(parametro1); // valor o 1
		console.log(parametro2); // valor o 1
	}
}

obj.func({
	parametro1: 23;
}) // Resultado sera 23, 1
```

