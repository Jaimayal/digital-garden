---
title: "OOP en JavaScript"
date: "2023-01-09 13:21"
tags: 
  - javascript
draft: true
---
El OOP en JavaScript esta implementado por prototipos, aun asi, sigue los cuatro principios basicos:
- Abstraccion. Trae los detalles relevantes ignorando lo que no nnos interesa
- Encapsulacion
- Herencia
- Polimorfismo

Existen tres forma de implementar el OOP basado en prototipos (delegacion) en JS:
- Constructores. Crear objetos desde una funcion
- ES6 Classes. Sintactic sugar que utiliza la anterior para crear pero que hace que resulte mas comodo usar la OOP
- Object.create(). La funcion mas rapida de vincuilar un objeto a un prototipo

## Funcion Constructor
Son funciones normales, la unica diferencia esque para llamar un constructor utilizamos "new".
```JavaScript
const Constructor = function(attribute1, attribute2) {
	this.attribute1 = attribute1;
	this.attribute2 = attribute2;
}

const object = new Constructor('Algo', 'Atributo');
```
Al utilizar esta forma ocurre lo siguiente:
1. Se crea un nuevo objeto
2. Se llama a la funcion constructora(con parametros y todo)
3. La keyword "this" se asigna a este objeto creado en el contexto de la funcion
4. El objeto se vincula a un prototipo
5. El objeto se retorna de la funcion

## Prototipos
Para resumir, una funcion (TODAS) siempre tienen una propiedad llamada "prototype", incluidas las funciones constructoras. Por defecto, una funcion constructora dara acceso a todos los atributos y metodos definidos en el prototipo a sus instancias.

```JavaScript
Person.prototype // Propiedad prototype de la funcion constructora Person.

Person.prototype.function = function () {
return 'Este es el resultado de un metodo';
}

const jaime = new Person();
console.log(jaime.function()); //
```

Haciendolo de esta forma, todos los objetos que tengan una instancia acceden a la funcion del prototipo. Asi mismo, cada uno de los objetos puede utilizar sus atributos dentro de los prototipos.