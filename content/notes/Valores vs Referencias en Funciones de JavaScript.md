---
title: "Valores vs Referencias en Funciones de JavaScript"
date: "2022-09-29 11:12"
tags: 
  - 
draft: true
---
Es importante entender como funciona el paso por valor y paso por referencia en JavaScript.

Cuando a una funcion se le pasa una referencia (una estructura de datos o un objeto) le estamos pasando la misma referencia que existe dentro de cualquier otro contexto que se utilice la misma.

Es decir, que si mutamos el objeto dentro de la funcion, lo mutaremos para quien sea que tenga la misma referencia (Es decir, a otros [[notes/JavaScript Execution Context]], en especifico, afecta a todos los [[notes/Scope]])
