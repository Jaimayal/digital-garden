---
title: "JavaScript Execution Context"
date: "2022-09-23 13:39"
tags: 
  - javascript
draft: true
---
### Definicion
Un Execution Context es como un contenedor en el cual pueden vivir todas las partes de un codigo de javascript, keywords, objetos, funciones (solo las cabeceras), variables, etc.

**Es un concepto analogo a un Stack Frame**
### Componentes
- Variable Environment. Aqui vive cualquier variable declarada en el contexto (let, var, const, funciones, argumentos actuales).
- Scope chain.
- *this* keyword.

### Funciones
Adentrandose mas sobre el conceptos de Execution Context es aplicado tras lograr la compilacion en el proceso de ejecucion dentro de un [JavaScript Engine](notes/JavaScript%20Engine.md).

1. Tenemos el codigo compilado y listo para ser ejecutado
2. Se crea el contexto global de ejecucion donde se ejecuta todo el codigo que esta fuera de cualquier funcion.
3. Se ejecuta todo el codigo dentro del contexto global de ejecucion.
4. Se ejecutan las funciones conforme se vayan llamando.
	1. Se llama una funcion
	2. Se crea un Function Execution Context, en donde podemos encontrar las variables locales, constantes, objetos, otras funciones, etc.
	3. Se agrega el FEC al Call Stack
	4. Se ejecuta el Call Stack siguiendo el LIFO.

GEC (Global Execution Context). Exactamente uno es creado para todo el codigo que no se encuentra dentro de ninguna funcion.

FEC (Function Execution Context). Uno es creado por cada funcion.