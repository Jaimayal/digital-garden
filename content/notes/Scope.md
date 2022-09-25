---
title: "Scope"
date: "2022-09-25 07:57"
tags: 
  - 
draft: true
---
Alcance que tiene una variable tomando en cuenta desde donde fue declarada. Pueden ser globales, de funcion o de bloque.

Por tanto si decimos el Scope de una Variable nos referimos a los espacios desde donde puede ser accedida

Scoping es el termino que se usa para referirse al orden y alcance que tiene cada una de las variables del codigo.

### Tipos
#### Global
- Son declaradas fuera de cualquier funcion
- Pueden ser accedidas desde cualquier parte del programa

#### Funcion
- Son declaradas dentro de una funcion
- Pueden ser accedidas solo desde dentro de una funcion
- Si se declaran variables con la keyword *var* estas siempre tendran scope de funcion, nunca de bloque.

#### Bloque
- Son declaradas dentro de un bloque de codigo, es decir, entre {}.
- Pueden ser accedidas solo desde dentro del bloque
- Solo sirve con las variables declaradas mediante *let* y *const*.

### Scope Chain
Un scope chain se refiere a la cadena de herencia que ocurre con los scopes (y su contenido, variables) cuando se tienen multiples estructuras anidadas. Este forma parte fundamental del [[notes/JavaScript Execution Context]]

La funcion interna tendra acceso a las variables de todos los scopes superiores a ella (incluyendo argumentos en [[notes/JavaScript]])..

![[files/ScopeChain.png]]

Al proceso que ocurre cuando una funcion trata de buscar una variable en sus scopes superiores se le llama *Variable Look-up*.