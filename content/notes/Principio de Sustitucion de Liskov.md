---
title: "Principio de Sustitucion de Liskov"
date: "2022-10-28 17:30"
tags: 
  - oop
draft: true
---
**Cualquier subclase debe sustituir de forma satisfactoria a una clase padre dentro de una jerarquia, sin cambiar de forma exagerada su comportamiento**

Es un principio que sirve para evaluar una Jerarquia de Clasificacion (herencia) y ver si es valido utilizarla en conjunto con sus colaboradores por un cliente.

Para que la Jerarquia sea dada como valida, un cliente deberia de poder utilizar una clase abstracta y cualquiera de sus derivadas, utilizar sus operaciones publicas y que todas ellas ejecuten su funcion.

Como sabemos que ejecuto su funcion correctamente?.
- Lo que **si esta permitido** esque la precondicion de las derivadas sea mas flexible que la precondicion de la base.
- Lo que **no esta permitido** esquie la postcondicion de la derivada sea mas flexible que la precondicion de la base

Si una clase derivada tontita se le ocurre violar las condiciones de arriba es mejor ni concebirla como funcional.

Es como el pinguino y el ave, no puede ser una jerarquia de clasificacion debido a que el pinguino limita las operaciones de ave porque no puede volar.

Como yo lo entiendo tambien indica que las jerarquias de herencia por limitacion y herencia por exclusion rompen este principio.

