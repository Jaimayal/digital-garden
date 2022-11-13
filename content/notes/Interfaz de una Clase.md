---
title: "Interfaz de una Clase"
date: "2022-10-28 14:16"
tags: 
  - oop
draft: false
---
La interfaz de una [[notes/Clase]] se refiere al conjunto de [[notes/Metodos]] que estan expuestos de forma publica para que otras clases desde cualquier otro paquete puedan colaborar con ella.

**Una buena interfaz publica debe de ser minima, ofreciendo los metodos suficientes (de forma homogenea) para que otros lleven acabo sus propias operaciones**

Por tanto, una buena clase debe ser:
- Homogenea. Nombrado, orden de parametros, valores de retorno
- Suficiente. Que no haya efectos secundarios, que solo sean acciones unicas.
- Minima. Que ofrezca la interfaz minima suficiente para satisfacer las necesidades basicas (primitivas) y nada mas.
## Smell Codes
### Codigo Sucio por Clases Alternativas con Interfaces Diferentes
Se debe homogeneizar el nombrado que se le da a las cosas de escencia similar dentro del codigo, tratar de mantener una terminologia homogenea en el como son nombrados los metodos publicos a traves de todas las clases es algo a lograr.

- Homogeneizar los nombres
- Utilizar herencia por extension o implementacion
- Mover responsabilidades

### Principios del Menor Compromiso
Una clase solo debe exponer en su interfaz publica los metodos suficientes como para que desarrolle su unico trabajo sin tener efectos secundarios o tener metodos que no van de acuerdo con el nombrado / los datos que tiene.

**Cada metodo tiene que ser un unico verbo, e implementa solo lo que dice**.

### Interfaz Suficiente, Completa y Primitiva
- Suficientes caracteristicas para satisfacer las funcionaldiades que debe proveer a otras clases
- Primitiva. Solo contener operaciones que son primitivas para esta clase y no requiere de muchas especificaciones.
