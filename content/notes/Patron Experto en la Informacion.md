---
title: "Patron Experto en la Informacion"
date: "2022-10-01 09:04"
tags: 
  - ooad
draft: true
---
Se dice que un objeto tiene obligaciones que son dadas por los datos que guarda. Sus obligaciones es ofrecer una interfaz publica que satisfasca las operaciones necesarias que otros objetos tienen que hacer con ese dato.

Pensar muy bien la relacion que existe entre el conocimiento que tiene una parte del sistema y las operaciones que hace con esos datos.

Es ilogico que un subsistma que busca persistir los datos haga calculos de cuanto tiempo tienen que durar en ella.

**Este es el principio general de la asignaciond e responsabilidades:**
> *Inspirate en el Mundo Real, pero se coherente y has que las clases hagan las operaciones que les corresponden con los datos que encapsulan.*

En pocas palabras, **asigna la responsabilidad que le corresponde a la clase que tiene la informacion necesaria para cumplirarla**. De ser necesario tener colaboradores, tambien se puede especificar
