---
title: "Intercambiar la Visibilidad de un Elemento usando JavaScript"
date: "2022-09-23 09:41"
tags: 
  - javascript
draft: false
---
Para saber como cambiar la visibilidad de un objeto en JavaScript primero debemos tener un poco de conocimiento sobre la [Manipulacion del DOM](notes/Manipulacion%20del%20DOM.md).

## Propiedades de CSS
Como sabemos, mediante la [Manipulacion del DOM](notes/Manipulacion%20del%20DOM.md) se pueden cambiar los estilos de cualquier bloque del documento HTML.

Existen dos propiedades particulares que nos dejaran cambiar la visibilidad de los elementos:

```CSS {title='Propiedad display'}
display: none;
display: block;
display: inline;
display: inline-block;
```

```CSS {title='Propiedad visibility'}
visibility: visible;
visibility: hidden;
```

## Aplicacion con JavaScript
Una vez conocemos las propiedades necesarias para ocultar y mostrar un elemento, su aplicacion con JavaScript seria la siguiente:

```JavaScript
document.querySelector('.clase').style.PROPIEDAD = 'VALOR';
```

En donde PROPIEDAD puede ser visibility o display y VALOR puede ser cualquiera de los valores respectivos para la propiedad.

Aqui hay un [codepen de demostracion](https://codepen.io/Jaimayal/pen/ZEoXxYB) que podria ser relevante.

### Codigo 
**Ocultar**
```JavaScript
document.querySelector('.selector').style.visibility = 'hidden';
```

**Mostrar**
```JavaScript
document.querySelector('.selector').style.visibility = 'visible';
```