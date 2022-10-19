---
title: "Metodo bind en JavaScript"
date: "2022-09-30 08:28"
tags: 
  - javascript
draft: false
---
Tal y como los metodos [[notes/Metodo apply en JavaScript]] y [[notes/Metodo call en JavaScript]], este tambien nos permite cambiar la keyword [[notes/this en JavaScript]] de lugar.

Sin embargo, esta funcion tiene un comportamiento diferente. En vez de llamar a la funcion directamente, **retorna una funcion en la cual la keyword this ya esta asignada de forma correcta**.

Esto nos sirve mucho para poder reutilizar el llamado de una funcion multiples veces para un objeto sin escribir tanto boilerplate code.

```JavaScript
const nuevaFuncionBindeada = funcion.bind(thisKeywordReplacment);
```

Sin embargo este funcion tambien permite asignar otros argumentos, la cuestion esque estos no podran ser cambiados a futuro

```JavaScript
const nuevaFuncionConArg = funcion.bind(thiskeywordrepl, arg1) // El valor de arg1 sera permanente cuando se llame nuevaFuncionConArg.
```

A esto se le llama **aplicacion parcial** debido a que algunos argumentos ya estaban colocados. Sirve como crear una plantilla y posteriormente crear otros tipos de funciones similar a ella pero cambiando menos argumentos.