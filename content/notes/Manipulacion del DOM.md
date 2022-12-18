---
title: "Manipulacion del DOM"
date: "2022-09-19 10:21"
tags: 
  - javascript
draft: false
---
La manipulacion del [DOM](notes/DOM.md) ocurre cuando utilizamos un lenguaje de programacion para interactuar de forma dinamica con un documento de HTML mediante el WEB API que ofrecen los navegadores.

Utilizando JavaScript existen muchas formas de manipularlo. Aqui algunas de ellas.


## Seleccionar elementos
Hay una forma especial de seleccionar todo el documento
### documentElement
Es un elemento especial del objeto document que sirve para seleccionar todo el documento HTML.

### document.head
Te permite seleccionar el head del HTML
### document.body
Te permite seleccionar el body del HTML

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



### querySelectorAll()
Tiene las mismas funciones y propiedades que querySelector solo que, en vez de seleccionar al primero, **selecciona todos los elementos con el selector especificado** y devuelve un NodeList (que funciona como un [Arrays en JavaScript](notes/Arrays%20en%20JavaScript.md)) con ellos dentro.



### getElementById
Recibe un id de un elemento del documento y lo devuelve. Tiene que ser un id especificamente
### getElementsByTagName
Recibe una etiqueta y te devuelve un HTMLCollection con todos los elementos que sean de esa etiqueta.

Un HTML Collection es afectada en tiempo real por cambios en el DOM

### getElementsByClassName
Recibe una clase y devuelve un HTMLCollection con todos los elementos que contengan ese nombre de clase.

## Crear e Insertar elementos
### insertAdjacentHtml()
Sirve para insertar html antes, dentro, antes de terminar y despues de la etiqueta de cierre de un elemento html, de esta forma, podemos agregar de manera dinamica elementos al DOM.

```JavaScript
const htmlElement = '<div class='hola'>hola</div>';

document.querySelector('.div1').insertAdjacentHtml('afterbegin', htmlElement);
```

### createElement()
Recibe el nombre de una etiqueta y retorna el elemento que peude ser agregado al DOM en cualquier punto.

La ventaja esque podemos modificar e ir agregando elementos conforme nos vaya pareciendo. Agregar clases, agregar otros elementos, agregar HTML, agregar estilos y todo lo que se puede modificar de un elemento HTML

### prepend()
Agrega un elemento HTML al inicio de la etiqueta (tras solo realizarla)

### append()
Agrega un elemento HTML como ultimo elemento de un contenedor

### cloneNode
Se puede aplicar con un elemento HTML y sirve para realizar una shallow y deep copy de un elemento. Necesario debido a la inmutabilidad de los elementos.

### before()
Inserta un elemento HTML antes de otro elemento HTML sobre el que se especifica el elemento

### after()
Inserta un elemento HTML despues de otro elemento HTML sobre el que se especifica el elemento

## Remover elementos
### remove()
Sirve para remover un elemento del DOM de HTML. Lo borra completamente

## Estilos
Para poder asignar los estilos tenemos que tener seleccionado un elemento utilizando cualquiera de los selectores disponibles.
### Inline
Tambien podemos cambiar los estilos de cualquier elemento de forma dinamica, esto se hace accediendo a la propiedad .style. Una vez hecho esto solo nos queda especificar una propiedad de CSS por cambiar:

```JavaScript
document.querySelector('.texto').style.color = '00fffff'; // Cambia la letra a color amarillo
```

### Clases
Otra forma (y la mas utilizada) de modificiar los estilos de una pagina web es agregar, remover y modificar las clases de un elemento, de esta forma, podemos agregar y remover un grupo de caracteristicas del elemento que busquemos. 

Para esto, cada elemento del documento cuenta con un objeto especial llamado **classList** que sirve para referirse al atributo de clases de la etiqueta HTML.

```JavaScript
document.querySelector('.button').classList.add('hidden'); // Selecciona el elemento con la clase 'boton', selecciona su lista de clases y agrega la clase 'hidden'
```

En este caso, si en el archivo CSS existen propiedades para la clase 'hidden' se aplicaran al elemento de forma dinamica.

### getComputedStyle
Es una funcion integrada que sirve para obtener los estilos computados de un elemento
```JavaScript
const element = document.querySelector('#btn');
getComputedStyle(element).style;
```

### CSS Variables
Tambien es posible cambiar las variables CSS que son definidas en un archivo es estilos.
```CSS
:root {
	--color-primary: red;
}
```

Para hacerlo, debemos acceder al documento root y cambiar esa propiedad. En JavaScript se haria utilizando la funcion setProperty.

```JavaScript
document.documentElement.style.setProperty('--color-primary', 'green');
```
## Atributos
Para cambiar los atributos de una etiqueta de HTML, primero se necesita elegirla utilizando cualquiera de los selectores.

### Como propiedades
Estos se encuentran definidos como propiedades de cualquier elemento HTML, por tanto, pueden ser accedidas utilizando la sintaxis del .

```JavaScript
const element = document.querySelector('#element');
element.id // id proeprty
element.className // class property
element.designer // undefined
```
Sin embargo, esto solo nos permite leer las propiedades que son esperadas de un elemento, por tanto, todos los atributos que no sean respectivos a un elemento no funcionaran de esta forma.

Esta sintaxis nos permite sobreescribir los valores de los atributos.
```JavaScript
element.id = 'newId';
```

### Metodos getAttribute y setAttribute
Existe un metodo especial de cualquier elemento HTML que nos sirve para obtener un atributo **aun cuando este no es parte estandar de los elementos definidos para esa etiqueta en particular**.

```JavaScript
element.getAttribute('designer'); // Jaime
```

Como es logico, el metodo setAttribute nos permite colocar valores y atributos a un elemento 

```JavaScript
element.setAttribute('company', 'Name');
```

### dataSet
Esta propiedad solo es aplicable para los data attributes que se pueden definir en un documento HTML.
```HTML
<div class="container" data-variable-mov="3.33">

</div>
```

```JavaScript
const element = document.querySelector('.container').dataset.dataVariableMov // 3.33
```

## Eventos
Un evento señaliza la ocurrencia de algo en el UI, el ejemplo mas comun es una interaccion con el usuario

Un EventListener nos sirve para escuchar un elemento y hacer algo con el. No cambia la ocurrencia de un evento, solo cambia la respuesta que tiene el codigo respecto a el.

### addEventListener
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
#### Eventos en el Teclado
Una de las funcionalidades mas basicas es interactuar con el usuario mediante el teclado, en una pagina web, se puede hacer mediante un eventListener.

Al tratarse del teclado, se debe declarar como un **event global**. Es decir, que ocurriran sin importar en que parte o momento de la pagina nos encontremos porque se encuentra embebido dentro del documento.

Veamos un ejemplo:

```JavaScript
document.addEventListener('keydown', (event) => {
	console.log(event);
})
```
### onEvent
Existe una propiedad especial para cada uno de los eventos disponibles en un elemento de HTML. Este recibe la sintaxis especial 'onX' donde X es el nombre del evento, ejemplos:

```JavaScript
element.onClick = //...
element.onMouseEnter = //...
```

Es una forma legacy de setear un evento, solo permite a una funcion ejecutarse por propiedad

### removeEventListener
Sirve para remover un event listener de ocurrir. Nos sirve para remover un comportamiento basado en otro evento.
