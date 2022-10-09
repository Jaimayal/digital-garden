---
title: "Manipulacion del DOM"
date: "2022-09-19 10:21"
tags: 
  - javascript
draft: false
---
La manipulacion del [DOM](notes/DOM.md) ocurre cuando utilizamos un lenguaje de programacion para interactuar de forma dinamica con un documento de HTML mediante el WEB API que ofrecen los navegadores.

Utilizando JavaScript existen muchas formas de manipularlo. Aqui algunas de ellas.

### querySelector()
Primeramente debemos obtener el objeto del documento html, y posteriormente llamar al metodo especial querySelector().

En el parametro del metodo querySelector debemos colocar un selector de la misma forma que lo hacemos en CSS. Un .nombre para clases un \#nombre para los IDs, etc etc.


```JavaScript
document.querySelector('.text'); // Seleccion del primer elemento con el nombre de clase 'text', por ejemplo, <p class='text'>Hola mi nombre es Jaime Ayala</p>
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
###### Informacion sobre el Evento
Es posible obtener informacion detallada sobre el evento en forma de un objeto, esto se hace poniendo un parametro dentro de la expresion funcional del eventListener:

```JavaScript
document.querySelector('.button').addEventListener('click', (event) =>
	console.log(event);
)
```
###### Eventos en el Teclado
Una de las funcionalidades mas basicas es interactuar con el usuario mediante el teclado, en una pagina web, se puede hacer mediante un eventListener.

Al tratarse del teclado, se debe declarar como un **event global**. Es decir, que ocurriran sin importar en que parte o momento de la pagina nos encontremos porque se encuentra embebido dentro del documento.

Veamos un ejemplo:

```JavaScript
document.addEventListener('keydown', (event) => {
	console.log(event);
})
```

### querySelectorAll()
Tiene las mismas funciones y propiedades que querySelector solo que, en vez de seleccionar al primero, **selecciona todos los elementos con el selector especificado** y devuelve un NodeList (que funciona como un [Arrays en JavaScript](notes/Arrays%20en%20JavaScript.md)) con ellos dentro.
### Estilos
#### Inline
Tambien podemos cambiar los estilos de cualquier elemento de forma dinamica, esto se hace accediendo a la propiedad .style de cualquier objeto del querySelector:

```JavaScript
document.querySelector('.texto').style;
```

Esto devuelve un objeto con todos los estilos del elemento al que seleccionamos, de modo que ahora, solo nos queda especificar una propiedad de CSS por cambiar:

```JavaScript
document.querySelector('.texto').style.color = '00fffff'; // Cambia la letra a color amarillo
```

#### Clases
Otra forma (y la mas utilizada) de modificiar los estilos de una pagina web es agregar, remover y modificar las clases de un elemento, de esta forma, podemos agregar y remover un grupo de caracteristicas del elemento que busquemos. 

Para esto, cada elemento del documento cuenta con un objeto especial llamado **classList** que sirve para referirse al atributo de clases de la etiqueta HTML.

```JavaScript
document.querySelector('.button').classList.add('hidden'); // Selecciona el elemento con la clase 'boton', selecciona su lista de clases y agrega la clase 'hidden'
```

En este caso, si en el archivo CSS existen propiedades para la clase 'hidden' se aplicaran al elemento de forma dinamica.

### insertAdjacentHtml()
Sirve para insertar html antes, dentro, antes de terminar y despues de la etiqueta de cierre de un elemento html, de esta forma, podemos agregar de manera dinamica elementos al DOM.

```JavaScript
const htmlElement = '<div class='hola'>hola</div>';

document.querySelector('.div1').insertAdjacentHtml('afterbegin', htmlElement);
```