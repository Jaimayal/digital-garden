---
title: "Modularidad"
date: "2022-10-24 11:26"
tags: 
  - oop
draft: false
---
Es un concepto que se refiere a la descomposicion de un programa en multiples modulos. Un modulo es una pieza de construccion, en la [[notes/Programacion Orientada a Objetos]], un modulo es una [[notes/Clase]]. 

El objetivo es contar con un numero de modulos balanceado en el cual se distribuyan las responsabilidades de con alta [[notes/Cohesion]] y poco [[notes/Acoplamiento]], respetando las heuristicas de [[notes/Granularidad]].

### Numero de Modulos
La cantidad de modulos por programa debe ser ajustada a la cantidad de codigo que tendra cada una.

Al realizar diseño modular existen dos costes principales.
- Costo por Implementacion. Lo que cuesta escribir cada clase (cantidad de lineas).
- Costo por Integracion. Lo que cuesta integrar todas las clases con un buen diseño.

![[files/CostoDeIntegracion.png]]

### Distribucion de Responsabilidades
El problema debe ser dividido entre distintos modulos de modo que todos aporten algo a resolver el problema de forma relativamente equitativa. Es decir, distribuir una gran responsabilidad de manera equilibrada entre multiples clases.
