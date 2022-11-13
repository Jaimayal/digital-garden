---
title: "Principio Open-Closed"
date: "2022-10-28 17:40"
tags: 
  - oop
  - solid
  - ooad
draft: false
---
Es el Objetivo del Diseño Orientado a Objetos.

Dicta que: **Todas las partes del paradigma orientaod a objetos deberian estar *abiertas a la extension, cerradas a la modificacion.**

Es decir, debemos lograr tal diseño que no tengamos que modificar nada para arreglar algo, unicamente para extender su funcionalidad.

Esto se hace teniendo dos partes
1. Una clase fija, que sirve como base y que es polimorfica
2. Multiples implementaciones dinamicas que pueden colgar de una referencia a una clase fija polimorfica

Por tanto, la clase fija SIEMPRE sera abstracta y el infinito numero de posibilidades extensibles son las clases concretas dinamicas.

El controlador se encarga del dialogo entre el actor y el sistema. Existe uno por cada caso de uso.

## Rupturas
- Prohibido el instanceof
- Prohibido atributos publicos
- Prohibidas las variables globales

DEBIDO A QUE ESTO NOS ACOPLA A LAS PARTICULARIDADES DETRAS DE UNA JERARQUIA POLIMORFICA.