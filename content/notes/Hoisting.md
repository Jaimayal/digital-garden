---
title: "Hoisting"
date: "2022-09-25 08:29"
tags: 
  - javascript
draft: true
---
Es un mecanismo de [[notes/JavaScript]] que sirve para manejar la creacion y flujo de las variables. Lo que hace esque **permite a algunas variables ser utilizadas antes de que sean declaradas**.

Como sabemos, en JavaScript se lee de arriba a abajo instruccion por instruccion, el Hoisting permite acceder a variables que se encuentran hasta abajo por lineas que se encuentran por arriba de esta.

## Funcionamiento
El codigo es escaneado por variables y para cada una se le crea un elemento que es agregado al *variable environment*.

### Funciones Declaradas
Este proceso es exactamente lo que ocurre con el primer tipo de funcion, las Funciones Declaradas ([[notes/Funciones en JavaScript]]).

### Variables con var
Por otro lado, este proceso tambien es aplicado a las variables que se declaran con *var*, sin embargo, al tratar de ser utilizadas antes de ser asignadas por la linea que deberia se le da el valor de 'undefined'. Este es una de las razones principales por la cual muchos bugs son introducidos a los programas.

### Variables con let/const

Finalmente, las variables declaradas con *let* y *const* no tienen hoisting de manera efectiva, si tratan de ser utilizadas ocurrira un error *Uninitialized*, es debido a que se encuentran en una zona muerta temporal hasta que llegan a la sentencia donde se les asigna su valor real.

### Expresiones Funcionales
La expresiones funcionales (o arrow functions) dependen del tipo de variable que se les asigna, let/const o var.

![[files/Hoisting.png]]