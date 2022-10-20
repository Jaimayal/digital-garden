---
title: "Recomendaciones en Funciones para mantener codigo limpio"
date: "2022-10-19 19:59"
tags: 
  - programming
  - ooad
draft: true
---
Debido a que las funciones son un concepto transversal que ha persistido casi desde la creacion de la disciplina de programacion, es importante conocer las heuristicas recomendadas para mantenerlas con codigo de calidad.

### Caracteristicas de una buena funcion
- Es pequeña
- No tiene muchos niveles de identacion
- Hace una sola cosa, la hace bien y solo esta la debe hacer.
- No necesita dividirse en bloques / secciones
- No tiene codigo repetido
- Utiliza Template Pattern de ser necesario
- Debe de tener un nombre lo suficientemente descriptivo como para saber que hace
- Debe de tener entre 0 a 3 argumentos maximo para que sea legible
- No debe contener banderas (flags) en forma de booleanos, tenerlas indica que se hacen dos acciones, una cuando es positivo y otra cuando es falso.
- Debe utilizar objetos como argumentos de ser necesario
- No debe de tener listas de argumentos
- No tienen efectos secundarios mas alla de lo que indica su nombre
- Son parte del comportamiento del objeto particular y trabajan con el de forma clara.
- Debe cambiar el estado de un objeto o debe devolver informacion. Solo una de ellas.
- Se separan de bloques try/catch lo maximo posible
- Se utilizan excepciones por sobre codigos de error particulares
- Siguen el principio DRY
- Cada funcion y bloque solo debe de tener un punto de entrada y uno de salida

