---
title: "Patron de Vista Separada"
date: "2022-10-28 16:58"
tags: 
  - ooad
draft: false
---
Es uno de los Patrones recurrentes que dio vida a la arquitectura MVC. Dicta que, los modelos como minimo deben estar desacoplados totalmente de la tecnologia de vista necesaria para interactuar con los usuarios, puesto que, de estar acoplados (Mediante el [[notes/Patron Experto en la Informacion]], por ejemplo) crearian clases que romperian con los principios de [[notes/Cohesion]], [[notes/Acoplamiento]] y [[notes/Granularidad]].

Nunca hagas un modulo que interactue con el usuario, comunicacion o que sea cualquier interfaz para cualquier canal externo. SEPARA LAS COMUNICACIONES, LA PANTALLA Y TUS MODELOS.

Todas las clases con System.out y todo deben ir en otra clase. Para trabajar con ficheros otra clase, para trabajar con GUI otra clase.

**Una vista es todo aquello que recibe, lee y valida la informacion que proviene de un sitio externo al software**. 
