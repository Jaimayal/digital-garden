---
title: "Patron de Indireccion"
date: "2022-10-28 16:55"
tags: 
  - oop
  - ooad
draft: false
---
Es un Patron que dicta que la Indireccion de la complejidad en la [[notes/Programacion Orientada a Objetos]] debe ocurrir mediante la creacion de mas clases. 

**TODOS LOS PROBLEMAS DE DISEÑO, DESACOPLAMIENTO, COHESION SE ARREGLAN AGREGANDO MAS CLASES.**

## Justificacion
Los niveles de abstraccion ayudan a reducir el acoplamiento de la cantidad de elementos con los que se trabaja.

Para agregar un nivel de abstraccion en codigo basta con agregar una clase y posteriormente utilizar su interfaz publica para ejecutar las operaciones de los elementos que engloba. 

No necesariamente se puede agregar una, se pueden agregar varias e incrementar la Cohesion, dividir un problema y dividir responsabilidades.

**Todo se resuelve con mas clases, que reduzcan las responsabilidades y reduzcan el acoplamiento**

## Patron de Invencion Pura
Debido a la necesidad de crear mas clases para redireccionar la complejidad de una clase. El Patron de Invencion Pura dicta que las clases ya no solo deben venir del modelo del dominio, sino que se deben de generar como clases de control y pueden venir de cualquier parte que nos inventemos.

Algunos ejemplares citados por otros autores pueden ser encontrados en las [[notes/Categorias de los Objetos (Clases) en Diseño]].

## Patron Creador
Debido a que, la solucion a los problemas de diseño (para lograr una buena cohesion con bajo acoplamiento y bajo tamaño) es agregar clases las cuales pueden venir del modelo o ser inventadas (Como las vistas y los controladres), el patron creador viene para resolver toda esa conglomeracion de creacion de objetos y clases que pueden hacer que un sistema se vuelva dificil de manejar.

- Factorias
- Builder

En el caso de una aplicacion de Spring.
- Lo comunmente llamado "Controller" (o donde recide toda la llegada de comunicacion mediante endpoints HTTP) es la Vista.
- Lo comunmente llamado "Service" (o donde recide toda la logica de negocio fuerte) es el controlador.

La capa Controller solo se encarga de recibir peticiones y remover todo lo relacionado con HTTP, al servicio nada mas le llegan los datos y el lo procesa, ni siquiera sabe que llegan por HTTP, bien podria ser cambiado por una app de Swing y no hay ningun problema.

- Vista, una por cada protocolo de comunicacion, interfaz o forma de recibir datos
- Controlador, uno por cada caso de uso que se necesitan
- Modelo, inspirados del modelo del dominio, datos duros

Inyeccion de Dependencias = Relacion por Asociacion
