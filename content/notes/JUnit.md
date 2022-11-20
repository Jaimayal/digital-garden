---
title: "JUnit"
date: "2022-11-20 08:56"
tags: 
  - 
draft: true
---
JUnit nos permite escribir pruebas con mucha facilidad y multiples pruebas para cada clase individual. Nos permite escribir tests rapido y provee informacion limpia sobre los errores metodos y lugares en los que fallo la aplicacion.

JUnit es una libreria que nos permite escribir y ejecutar pruebas. 

## JUnit 5
Es la ultima actualizacion que ocurrio de JUnit la cual integra muchas funcionalidades de Java 8 y versiones posteriores. 

Es decir, JUnit 5 portrae soporta para programacion funcional, lambdas, nuevas anotaciones, un ciclo de vida y demas configuracion.

Implementa una nueva arquitectura robusta en la cual se tienen distintos componentes. Entre ellos tenemos:
- JUnit Platform. Libreria principal orientada a la ejecucion de pruebas. Esto permite que las pruebas esten escritas con JUnit Jupiter o cualquier otra que interactue con la JUnit Platform.
- JUnit Jupiter. Componente que permite a los desarrolladores escribir sus pruebas mediante codigo y ejecutarlas en la JUnit Platform
- JUnit Vintage. Componente que permite preservar pruebas escritas en versiones anteriores de JUnit.

Con la anotacion @Test marcamos una pieza de codigo para que sea ejecutada en la JUnit Platform

Un import static nos sirve de la clase Assertions nos sirve para traer todos los metodos de aserciones para comprar un elemento esperado con un elemento real que se generado por la ejecucion de un metodo.

Para cada test se crea una nueva instancia 