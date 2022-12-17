---
title: "DOM"
date: "2022-09-19 10:05"
tags: 
  - javascript
draft: false
---
El DOM se refiere al Document Object Model. El DOM es una representacion estructurada de un documento HTML, mediante este, podemos cambiar de forma dinamica los estilos y el contenido de los elementos de una pagina web.

Sirve como interfaz para comunicar JavaScript con el navegador y permitir que los efectos sean posibles.

El punto de entrada para obtener el documento HTML en forma de objeto en Javascript es utilizar 'document.'

Es representado con una estructura de arbol y permite representar **absolutamente todo lo que se encuentre en el documento de HTML**.

![files/DOMTreeExample.PNG](files/DOMTreeExample.PNG)

**La especificacion del DOM no esta incluida en JavaScript**, esta implementada mediante un WEB API comun en todos los navegadores web, es por eso que no se necesita instalar ni descargar nada. 

## Como funciona

- Te permite interactuar con el usuario atraves del navegador
- Permite utilizar codigo de JavaScript para crear modificar, agregar, remover y listar distintos elementos, estilos, etiquetas y eventos que ocurran en el DOM.
- El DOM viene generado del documento html

## Tipos de Nodos
Algunos son elementos de HTML y otros son texto plano

## Organizacion del DOM API
Todos los nodos son del tipo *Node*, este es representado como un objeto, el cual tiene sus propiedades

Los nodos a su vez se pueden subdividir en categorias
- Element. El elemento mismo
- Text. Se encuentra dentro de un nodo
- Comment. Comentarios en HTML
- Document. El documento HTML entero

A su vez, cada elemento se compone internamente por un tipo de HTMLElement, puede ser HTMLButtonElement, HTMLDivElement, HTMLFormElement, etc. Cada uno de ellos tiene sus propias propiedades y atributos.

![[files/FuncionamientoDOMAPI.png]]