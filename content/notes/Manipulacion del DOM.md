---
title: "Manipulacion del DOM"
date: "2022-09-19 10:21"
tags: 
  - javascript
draft: true
---
La manipulacion del DOM ocurre cuando utilizamos un lenguaje de programacion para interactuar de forma dinamica con un documento de HTML mediante el WEB API que ofrecen los navegadores.

Utilizando JavaScript existen muchas formas de manipularlo. Aqui algunas de ellas.

### querySelector()
Primeramente debemos obtener el objeto del documento html, y posteriormente llamar al metodo especial querySelector().

En el parametro del metodo querySelector debemos colocar un selector de la misma forma que lo hacemos en CSS. Un .nombre para clases un \#nombre para los IDs, etc etc.


```JavaScript
document.querySelector('.text'); // Seleccion de las tags con el nombre de clase 'text', por ejemplo, <p class='text'>Hola mi nombre es Jaime Ayala</p>
```

#### Propiedades de un Elemento
Recordemos que se maneja en estructura de arbol, por tanto, debemos especificar que parte del objeto con clase 'texto' queremos, en este caso, veamos su contenido textual:

##### .textContent
```JavaScript
console.log(document.querySelector('.text').textContent); // Hola mi nombre es Jaime Ayala
```

Aparte de poder leerla, tambien podemos sobreescribirla como si fuera una variable:

```JavaScript
document.querySelector('.text').textContent = 'Hola me llamo Jaime'; // Actualizacion del elemento con la clase 'text'
```

#### Funciones de un Elemento

Como sabemos ahora, **los elementos de un objeto no solo son propiedades, si no que tambien pueden ser metodos**!. Por eso, tras seleccionar una etiqueta del documento podemos agregarle cosas como un escuchador de eventos para reaccionar a lo que hace el usuario.

##### .addEventListener()
Veamos un boton que al ser presionado actualiza el valor de nuestra etiqueta texto mediante el metodo .addEventListener:

```JavaScript
document.querySelector('.button').addEventListener('click', () =>
													  document.querySelector('.text').textContent = 'Presionado!';
												  )
```

El primer parametro de este metodo es el **tipo de evento al que esta escuchando** y el segundo la **expresion funcional (funcion anonima) que ejecutara cuando sea detectado**. En este caso utilice una arrow function.