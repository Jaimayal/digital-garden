---
title: "Cohesion"
date: "2022-10-22 14:53"
tags: 
  - softwaredev
draft: false
---
Es una medida que nos sirve para determinar que tantas responsabilidades tiene un modulo y que tanto se relacionan entre ellas.

> ***Una clase con alta cohesion tiene las responsabilidades minimas estrechamente relacionadas. Es decir, tiene un minimo numero de metodos altamente relacionados entre si***.

Este elemento es fundamental, se encuentra en todos lados, las nuevas arquitecturas de microservicios por ejemplo, en el que cada uno es dedicado a cierta funcionalidad exponiendo la minima cantidad de cosas que se relacionan estrechamente entre si.

## Objetivos
- Pocas funcionalidades
- Altamente relacionadas

___
Complejidad en el interior del modulo.

Representa la claridad de sus responsabilidades

Una tarea, proposito claro (high)

Encapsula multiples propositos o no tiene proposito claro (low)

