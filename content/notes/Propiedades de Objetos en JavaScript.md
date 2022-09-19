---
title: "Interacciones con Objetos en JavaScript"
date: "2022-09-19 08:11"
tags: 
  - javascript
draft: false
---
Existen dos formas basicas de interactuar con [Objetos en JavaScript](notes/Objetos%20en%20JavaScript.md) y cambiar o obtener sus propiedades.

### Notacion con Punto (Member Access)
Se especifica el nombre de la propiedad REAL que guarda el objeto y que se quiere obtener.

```JavaScript
object.propiedad;
```

Se utiliza de forma general debido a que es la forma mas clara de obtener datos.
### Notacion con Corchete (Computed Member Access)
Se especifica mediante una expresion el nombre de la propiedad que se desea obtener.

```JavaScript
const word = 'sion'

object['expre' + word];
```

Se utiliza cuando se necesita computar en una funcion o en otro lado el nombre de la propieda a obtener.

Estas dos notaciones pueden ser utilizadas no solo para acceder a elementos de un objeto, si no para mutarlo y agregar nuevos pares a el:

```JavaScript
const object = {
	name: 'Jaime',
	lastName: 'Ayala'
}

console.log(object.age) // Undefined

object.age = 2022 - 2002;

console.log(object.career) // Undefined

object['career'] = 'IT'

console.log(object.age) // 20
console.log(object.career) // IT

console.log(`${jonas.firstName} has ${jonas.friends.length} friends, and his best friend is called ${jonas.friends[0]}`);
```

