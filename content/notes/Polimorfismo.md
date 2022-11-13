---
title: "Polimorfismo"
date: "2022-10-28 17:59"
tags: 
  - oop
draft: false
---
El polimorfismo es una relajacion del sistema de tipos que nos permite interactuar con una clase y con todos sus derivados no abstractos apegandonos de forma fiel a su interfaz publica.

## Teoria de Lenguajes
**Enlace estatico, tiempo de compilacion**. toda aquella caracteristica que se pueda resolver mirando el codigo, viendolo. Aqui entran las checked exceptions.

**Enlace dinamico, tiempo de ejecucion**. lo contrario, esta caracteristica no se puede saber quien es hasta que se esta ejecutando la sentencia. Aqui entra el polimorfismo. Aqui entran las unchecked exceptions

Expresion combinacion de operadores y operandos que se evaluan devolviendo un unico valor.

Sin polimorfismo es un enlace estatico puesto que en todo momento sabemos el tipo del valor de retorno. Lo unico que podemos utilizar es sobrecarga.

Con polimorfismo tenemos un enlace dinamico puesto qu eno sabemos el tipo de valor real del retorno hasta que se ejecuta. Cada uno tendra comportamientos diferentes ya sea el original implantado o el de cualquiera de sus descendientes.

### Operaciones Polimorficas
Lo anterior mismo puede mandar con comunicacion entre clases con mensajes. Mientras una expresion me prometa que me devuelve A yo no se si me va a devolver A realmente o alguno de sus subclases.
