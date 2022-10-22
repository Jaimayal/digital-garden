---
title: "Acoplamiento Eferente"
date: "2022-10-22 15:04"
tags: 
  - softwaredev
draft: true
---
¿De quién dependo para realizar mi funcion?. Se identifica mediante las [[notes/Relaciones entre Clases (Gestion de Dependencias)]] y por el [[notes/Acoplamiento Indirecto]]. Es necesario reducir este acoplamiento al minimo, tenerlo demasiado indica una muy baja [[notes/Cohesion]],

Algunos casos de ella es:
- Cuando esta clase es la que usa a otras en una relacion de uso
- Cuando esta clase es el todo en una relacion de composicion
- Cuando esta clase es la que requiere de un asociado en una relacion de asociacion
- Cuando esta clase es hija de una superclase.
- Cuando ocupo metodoso de clases que no me corresponden (Romper la Ley de Demeter)

