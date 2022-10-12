---
title: "Diseño orientado a Objetos"
date: "2022-09-20 08:44"
tags: 
  - ooad
  - oop
draft: true
---
Nivel siguiente al [Diseño Modular](notes/Dise%C3%B1o%20Modular.md), ahora ya no solo son piezas bien inspiradas, legibles, poco acopladas y cohesivas, si no que se aprovechan los mecanismos de Polimorfismo y Herencia + Composicion para hacer jerarquias altamente reusables y flexibles respetando principios de la programacion orientada a objetos.

Contempla:
- Principio Open/Closed
- Principio de Sustitucion de Liskov
- Principio de Separacion de Interfaces
- Principio de Inversion de Dependencias

La herencia tiene la misma reusabilidad que una composicion.

La herencia te acopla fuertemente a la interfaz de tu padre y a sus atributos. Solo se pueden agregar atributos y metodos y redefinir metodos, nada mas.

El polimorfismo es una relajacion del sistema de tipos que nos permite interactuar con una clase y con todos sus derivados no abstractos apegandonos de forma fiel a su interfaz publica.

## Teoria de Lenguajes
Enlace estatico, tiempo de compilacion. toda aquella caracteristica que se pueda resolver mirando el codigo, viendolo. Aqui entran las checked exceptions.

Enlace dinamico, tiempo de ejecucion. lo contrario, esta caracteristica no se puede saber quien es hasta que se esta ejecutando la sentencia. Aqui entra el polimorfismo. Aqui entran las unchecked exceptions

Expresion combinacion de operadores y operandos que se evaluan devolviendo un unico valor.

Sin polimorfismo es un enlace estatico puesto que en todo momento sabemos el tipo del valor de retorno. Lo unico que podemos utilizar es sobrecarga.

Con polimorfismo tenemos un enlace dinamico puesto qu eno sabemos el tipo de valor real del retorno hasta que se ejecuta. Cada uno tendra comportamientos diferentes ya sea el original implantado o el de cualquiera de sus descendientes.

### Operaciones Polimorficas
Lo anterior mismo puede mandar con comunicacion entre clases con mensajes. Mientras una expresion me prometa que me devuelve A yo no se si me va a devolver A realmente o alguno de sus subclases.

- Prohibido el instanceof
- Prohibido atributos publicos
- Prohibidas las variables globales

DEBIDO A QUE ESTO NOS ACOPLA A LAS PARTICULARIDADES DETRAS DE UNA JERARQUIA POLIMORFICA.

## Principio Open/Closed
Es el Objetivo del Diseño Orientado a Objetos.

Todas las partes del paradigma orientaod a objetos deberian estar **abiertas a la extension, cerradas a la modificacion.**

Es decir, debemos lograr tal diseño que no tengamos que modificar nada para arreglar algo, unicamente para extender su funcionalidad.

Esto se hace teniendo dos partes
1. Una clase fija, que sirve como base y que es polimorfica
2. Multiples implementaciones dinamicas que pueden colgar de una referencia a una clase fija polimorfica

Por tanto, la clase fija SIEMPRE sera abstracta y el infinito numero de posibilidades extensibles son las clases concretas dinamicas.