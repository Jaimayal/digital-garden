---
title: "Desarrollo Top-Down"
date: "2022-10-24 11:32"
tags: 
  - oop
  - programming
draft: true
---
Es un metodo de desarrollo que sirve para escribir programas simples de forma ordenada, manteniendo en todo momento los conceptos de [[notes/Cohesion]], [[notes/Modularidad]] y [[notes/Granularidad]].

La metodologia es la siguiente:
1. Se elabora un Diagrama de clases base en donde existan las clases principales y sus relaciones mas basicas
2. Se selecciona una clase (Si es la primera, la clase base, si no, la que parezca mas dificil)
3. Se escriben sus atributos privados 
4. Se escribe su interfaz publica
5. Se implementan los metodos de la interfaz
6. Se instancian objetos y se usan metodos conforme sean necesarios de otras clases.
7. Se evalua y actualiza el diagrama
8. Se selecciona la clase mas riesgosa (aparentemente mas dificil) de escribir
9. Se vuelve al paso 2 hasta terminar

- 
