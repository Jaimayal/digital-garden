---
title: "Eventos en JavaScript"
date: "2022-12-18 09:20"
tags: 
  - javascript
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

Con el objeto event que se recibe en un event listener podemos obtener algunas propiedades importantes

```JavaScript
e.target // El elemento que trigereo originalmente el evento
e.currentTarget // El elemento actual por el que esta pasando el evento con bubbling seguramente

e.stopPropagation();
```

Adicionalmente, podemos detener la propagacion a cualquier elemento que busquemos, realmente usarlo es una mala practica pero es posible usarlo

Un eventListener usualmente actua sobre la fase de target y bubbling, es decir que la fase de captura no ejecuta nada, sin embargo, podemos pasa run tercer parametro a una funcion para que esta actue en la fase de captura en vez de la de bubbling
```JavaScript
element.addEventListener('click', function, true) // Hara que se ejecute la funcion en este elemento por captura y no por bubbling
```

Utilizando el mecanismo de Event Propagation podemos aprovecharnos de la delegacion de eventos. Mediante esta, podemos asignar un evento comun a un padre y que mediante el bubbling y el atributo e.target saber que fue lo que activo el evento. De esta forma, podemos hacer que con un solo eventlistener lidiemos con todos los eventos comunes que ocurran en sus hijos.