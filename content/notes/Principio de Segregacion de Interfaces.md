---
title: "Principio de Segregacion de Interfaces"
date: "2022-10-28 17:42"
tags: 
  - oop
draft: true
---
Es un principio que dicta que una clase no debe conocer nada mas alla de lo que le compete con otra clase con la que colabora.

Es decir, solo deben de tener la minima cantidad de metodos de modo que puedan comunicarse y hablar entre ellos.

Imaginando que un Alumno interactua con un Profesor mediante su interfaz Profesor y no conoce sus otras interfaces de Padre, Hermano, Hijo que forman parte de el y con la que otros interactuan, el solo conoce la de Profesor.

Otro ejemplo con una Secretaria se veria asi:

![[files/SegregacionInterfaces.png]]

Es como agregar otro nivel de abstraccion para que un cliente de una clase solo conozca las operaciones minimas.
