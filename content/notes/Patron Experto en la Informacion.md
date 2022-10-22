---
title: "Patron Experto en la Informacion"
date: "2022-10-01 09:04"
tags: 
  - ooad
draft: false
---
Es una heuristica que dicta que **un objeto tiene obligaciones que son dadas por los datos que guarda**. Sus obligaciones deben ser cumplidas y debe proveer interfaz publica para hacerlas accesibles a otros objetos desde fuera. Por tanto, podemos decir que esta fuertemente asociado al [[notes/Principio General de Asignacion de Responsabilidades]].

Para realizarlo bien se debe de pensar la relacion que existe entre el conocimiento que tiene una parte del sistema y las operaciones que hace con esos datos. Para apoyar este proceso se pueden utilizar Diagramas UML o [[notes/Tarjetas CRC]]

En pocas palabras, **asigna la responsabilidad que le corresponde a la clase que tiene la informacion necesaria para cumplirarla**. De ser necesario tener colaboradores (hacer una [[notes/Composicion]]), tambien se puede especificar

## Abuso del Patron Experto en la Informacion
Hay que tener una cosa en consideracion, a pesar de que la heuristica pueda sonar razonable, como todo, es importante no llevarlo al extremo.

En caso de ser llevado al extremo puede ocasionar que una clase llegue a tener un acoplamiento excesivo, a pesar de ser la que contiene los datos, debe utilizar colaboradores para delegar las tareas y que no tenga que hacer todo.

Un ejemplo seria la clase Alumno, que conoce sus datos y ademas de eso tiene que persistirse, imprimirse por pantalla, enviarse en comunicaciones TCP y otras mas cosas. 

### Consecuencias
- Rompes completamente el Principio Open/Closed debido a que tu clase se vuelve poco flexible y nada reusable.
- Rompes completamente los principios del [[notes/$ Diseño Modular]]



