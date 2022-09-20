---
title: "Antipatron Descomposicion Funcional"
date: "2022-09-20 11:47"
tags: 
  - ooad
draft: true
---
Tambien llamado **Functional Descomposition**, concepto creado por William Brown, se refiere a una mala practica que puede ocurrir en el desarrollo de un programa que consiste en romper completamente el [[notes/Principio General de Asignacion de Responsabilidades]].

Algunos sintomas son:
- Clases con un solo metodo 
- Ausencia de herencia y polimorfismo
- Clases con muchos miembros estaticos
- Datos saltando entre metodos

Las consecuencias son:
- Codigo poco mantenible, es decir, no reusable, no probable, no legible y no evolucionable. 

Lleva a tener un mal [Analisis y Disenio](notes/Analisis%20y%20Disenio.md), a empeorar los [Fundamentos de la Programacion](notes/Fundamentos%20de%20la%20Programacion.md) y por tanto, hacer el software mucho mas complejo.
