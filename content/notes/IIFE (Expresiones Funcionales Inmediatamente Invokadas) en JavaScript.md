---
title: "IIFE (Expresiones Funcionales Inmediatamente Invokadas) en JavaScript"
date: "2022-09-30 10:12"
tags: 
  - javascript
draft: true
---
Permite invocar una funcion anonima inmediatamente que se carga la pagina, de modo que no requiere de invocacion ni de ningun otro mecanismo.

Es utilizada invocando una Expresion Funcional directamente despues de ser declarada

```JavaScript
(function () {
	console.log("Starting...");
})();
```

1. La funcion anonima es cubierta con parentesis para convertirla en una funcion como si fuese ya asignada
2. Es invocada directamente sin ningun argumento ().

Esta funcion no podra volver a ser invocada en todo el script puesto que no tiene un nombre y se ejecutara inmediatamente que cargue la pagina.

De este modo podemos tener una inicializacion dentro de una funcion (la cual tiene su propio [[notes/Scope]]) y por tanto, sus variables y otras funciones no estan disponibles fuera de ella de modo que hace el codigo mas limpio.