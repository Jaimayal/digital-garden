---
title: "Principio General de Asignacion de Responsabilidades"
date: "2022-09-20 09:28"
tags: 
  - ooad
draft: true
---
> *Inspirate en el Mundo Real, pero se coherente y has que las clases hagan las operaciones que les corresponden con los datos que encapsulan.*

En pocas palabras, **asigna la responsabilidad que le corresponde a la clase que tiene la informacion necesaria para cumplirarla**. De ser necesario tener colaboradores, tambien se puede especificar

Por ejemplo, es ilogico que un subsistma que busca persistir los datos haga calculos de cuanto tiempo tienen que durar en ella.

Tambien buscar evitar clases get, get get get, set set set set, clases de datos vacias sin ningun comportamiento