---
title: "Cateogiras de los Objetos en Diseño"
date: "2022-10-21 19:46"
tags: 
  - softwaredev
draft: false
---
En el diseño, los objetos y tareas deben ser descritos en terminos de objetos, usualmente, estos se traducen a otros de granularidad mas pequeña. Los tres principales que podemos encontrar en todo diseño son:
- Entidades. Parte del Dominio
- Bordes. Fuentes de Informacion
- Control. Cumplir Open/Closed

## Objetos (Clases) Entidad (Entity)
Son los primeros en aparecer tras realizar los [[notes/Diseños Conceptuales y Tecnicos al Construir Software]]. De ellos, usualmente surgiran el resto de objetos que van mas orientados a la construccion tecnica del software.

Estos objetos entidad representan algo concreto y real del dominio del software. Pueden ser un usuario, un cliente, una cita. Al ser objetos estos contaran con sus datos y operaciones correspondientes.

## Objetos (Clases) Boundary
Son los objetos que surgen tras interacciones con sistemas externos, los cuales, deben estar desacoplados de las entidades iniciales del dominio del problema.

Usualmente, ellos se encargan de traer datos desde algun lugar, puede ser el internet, una API, un usuario (frontend), una base de datos o cualquier otro lugar que pueda servir como fuente de informacion.

Se relaciona mucho con las capas DAO, Repositorios y las vistas frontend, swing, console o cualquier otra.

## Objetos (Clases) de Control
Son los objetos que aparecen al buscar implementar un diseño de mejor nivel. Suelen controlar y orquestar a los demas objetos para garantizar un desacoplamiento entre ellos y que todos peudan trabajar de forma simple y clara.

Yo lo relaciono mucho con los objetos obtenidos por aplicar el Patron de Invencion Pura, Patron de Indireccion y Patron Controlador, etc. 
