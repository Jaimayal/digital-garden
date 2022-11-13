---
title: "Acoplamiento Aferente"
date: "2022-10-22 15:02"
tags: 
  - softwaredev
draft: false
---
¿Qué tanto se reusa mi clase?. Esa es la pregunta que se debe hacer para determinar la cantidad de acoplamiento Aferente. Se debe de tener especial cuidado, si se trata de una clase muy poco estable, que tiende a cambiar, es mas recomendado mirar en mecanismos dados por [[notes/Patrones de Diseño]] u otros.

Los casos especificos donde se da es:
- Cuando esta clase es la usada en una relacion de uso
- Cuando esta clase es una parte de una relacion de composicion
- Cuando esta clase es el asociado en una relacion de asociacion
- Cuando esta clase es padre de otras clases.
