---
title: "Diseños Conceptuales y Tecnicos al Construir Software"
date: "2022-10-21 18:12"
tags: 
  - softwaredev
draft: true
---
Son dos tipos de diseños que sirven para establecer de forma clara los componentes de un Software. Se establecen mediante los requisitos.

Un componente puede ser un conjunto de funciones, de clases, un paquete o un subsistema entero.

## Diseño Conceptual
En el, se utilizan los distintos casos de uso o requisitos para extraer los componentes principales que tendra el requisito en particular.

Por ejemplo. *Crear una barra de busqueda de Comida*. Los componentes de esta serian
- Barra de Busqueda
	- Buscar()
- Pagina de Resultados de Busqueda
- Comida
	- Ingredientes
	- Receta

## Diseño Tecnico
En el se empiezan a establecer los detalles importantes (relaciones, metodos, algoritmos) de cada uno de los componentes obtenidos en el diseño anterior. 

Siguiendo el ejemplo,
- Que algoritmo de busqueda que se ocupa
- La barra debe estar en todas las paginas o no
- La barra necesita o no abrir una nueva pagina con resultados de busqueda
- Que detalles se deben de mostrar de una receta

