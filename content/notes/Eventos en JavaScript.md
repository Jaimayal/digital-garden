---
title: "Eventos en JavaScript"
date: "2022-12-18 09:20"
tags: 
  - 
draft: true
---

Los eventos en JavaScript suelen tener tres fases especiales en las cuales se propagan a traves del DOM Tree.
1. Capturing
2. Target
3. Bubbling

Esto es debido a que los eventos se suelen generar en el elemento root del documento HTML.

La fase de captura es aquella en la que el evento va descendiendo desde el elemento root hasta el elemento donde ocurrio el evento. En caso de ser necesario, tambien se pueden agregar eventlisteners a esta fase

La fase de target es cuando se llega el elemento en el que ocurrio el evento y es donde usualmente se empiezan e ejecutar los eventlisteners para que ocurran interacciones con el usuario

La fase de bubbling es cuando el evento vuelve a regresar por su camino a traves de todos los elementos padres hasta llegar nuevamente al root. usualmente aqui tambien se atacan eventlisteners para que otros eventos ocurran

![[files/EventPropagationJS.png]]

De este modo, tenemos un ciclo de vida de los eventos en JavaScript, con una pre, fase y post.