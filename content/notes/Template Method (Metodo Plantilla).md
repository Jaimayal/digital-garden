---
title: "Template Method (Metodo Plantilla)"
date: "2022-10-28 17:54"
tags: 
  - oop
draft: true
---
Es utilizado en una Jerarquia de herencia. Se utiliza cuando dos clases derivadas tienen partes similares dentro del algoritmo de un metodo cambiando solo una pequeña parte debido a los detalles de su especializacion.

Lo que se hace es mover el codigo comun de ese metodo a la clase padre y definir un metodo abstracto para que los detalles que cambian sean redefinidos por las clases hijas.
