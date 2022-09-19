---
title: "Funciones en JavaScript"
date: "2022-09-18 15:14"
tags: 
  - javascript
draft: false
---
Existen tres tipos de funciones principales en JavaScript:
- Funciones Declaradas
- Expresiones Funcionales
- Funciones Flecha

Todas estas funciones cuentan con dos caracteristicas principales:
- nombre (que sirve para invocar, ejecutar o llamar la funcion)
- parametros 

### Funcion Declarada
Es un tipo de funcion declarada con el keyword ```function```, su caracteristica especial esque puede ser utilizada aun antes de ser declarada.

```JavaScript
nombreFuncion('Jaime');

function nombreFuncion(parametro) {
	console.log(`hola! ${parametro}`);
}
```

### Expresiones Funcionales
Una expresion funcional es simplemente una funcion anonima, en JavaScript es guardada en una variable para tener una forma de invocarse.

Su caracteristica esque necesitan ser definidas antes de ser utilizadas en el codigo

```JavaScript
const nombreFuncion = function (parametro) {
	console.log(`hola! ${parametro}`);
}

nombreFuncion()
```

### Funciones Flecha
Debido a la existencia de funciones anonimas,, se nos permite crear expresiones mas cortas (tipo lambdas en Java) que sirven para simplificar el codigo. En JavaScript son llamdas *arrow functions* y se utiliza del operador especial ```=>```.

```JavaScript
const nombreFuncion = parametro => console.log(`hola! ${parametro}`);
```

