---
title: "Diseño Modular"
date: "2022-09-20 08:42"
tags: 
  - ooad
  - programming
draft: false
---
Es el nivel posterior al [Diseño en Codigo](notes/Dise%C3%B1o%20en%20Codigo.md), aparte de ser codigo bien inspirado del modelo del dominio que es altamente legible, se agrega que son modulos (o piezas) de codigo que tienen un tamaño homogeneo con alta cohesion y poco acoplamiento. 

Es decir, piezas que tienen un tamaño similar, en el cual cada una ejerce una sola y unica funcion que se acopla con muy pocas piezas porque no es un experto que tiene que realizar todo en la aplicacion.

Para hacerlo aprovecha e impulsa la abstraccion, encapsulacion, modularidad y jerarquia, busca finalmente crear modulos de alta calidad, es decir, que tengan alta [Mantenibilidad](Mantenibilidad.md)] (escalabilidad, calidad, reusabilidad, etc).

## Criterios
Esta disciplina del diseño recupera tres conceptos recurrentes.
- [[notes/Cohesion]]
- [[notes/Acoplamiento]]
- [[notes/Granularidad]]

Una buena aplicacion de estos criterios resulta en clases altamente cohesivas y pocamente acopladas (acoplamiento eferente a clases inestables), con un bajo tamaño. Es decir, respetando al maximo el KISS.

## Consideraciones
- Hacer una buena [[notes/Interfaz de una Clase]]
- Promover el [[notes/Diseño por Contrato]] (Especialmente las precondiciones mediante asserts)
- Hacer una buena [[notes/Implementacion de una Clase]]

## Sugerencias
- Seguir el [[notes/Patron de Indireccion]]
- Implementar Vistas ([[notes/Patron de Vista Separada]])
- Implementar Controladores ([[notes/Patron Controlador]])
