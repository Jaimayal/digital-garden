---
title: "Relaciones entre Clases por Herencia"
date: "2022-09-26 11:29"
tags: 
  - oop
draft: false
---
Es un tipo de relacion que existe entre dos clases cuando se identifican factores en comun. Se obtiene una clase de mas alto nivel y se crea una pequeña jerarquia.

Response al acronimo *es un*:
- A es un B ?

## Herencia por Especializacion
Se tiene una clase padre que tiene elementos comunes, sin embargo, las clases hijas se especialziaran con unas operaciones sobre sus propios datos 

Rectangulo es una Figura ?
## Herencia por Extension
La clase base es un concepto mas abstracto que las clases hijas. Las clases hijas extienden mas el concepto del que heredan, añaden mas operaciones y lo extienden

Una correa tiene operaciones para sostener cosas, una correa de perro tiene las mismas operaciones que una correa pero con distinto tamaño, de otro material, etc.

## Herencia por Limitacion
La clase base tiene un conjunto de operaciones abstractas que deben ser implementadas por las clases hijas y estas no la implementan porque simplemente no cuentan con esa posibilidad

Es una herencia completamente desaconsejada y puede ser resuelta utilizando ... 

Un ejemplo seria la clase base Ave la cual tiene un metodo volar y la clase hija pinguino que como no puede volar no implementa el metodo

## Herencia por Construccion
La clase base es en realidad una parte (es decir, una composicion) de la clase hija y se trata de forzar una herencia.

Es un aherencia completamente desaconsejada debido a que incrementa la complejidad de como se ve un sistema.