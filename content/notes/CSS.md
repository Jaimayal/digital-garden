---
title: "CSS"
date: "2022-12-09 08:06"
tags: 
  - programming
draft: true
---
Cascade Style Sheet. Es un lenguaje que sirve para darle estilos a un lenguaje de marcado (regularmente y lo mas comun, HTML).

Este lenguaje esta compuesto de tres elementos principales:
- Selector
- Propiedad / Atributo
- Valor

## Selector
Es una forma dentro de una hoja de estilos que nos sirve para referirnos a un bloque de etiquetas en particular. 

```CSS
h2 {} /*El selector aqui es h2*/
```

Una forma de pensar en ellos es como queries. Debido a que hacen busqueda dentro del HTML en busqueda de los distintos selectores especificos para aplicar al documento.

### Basicos
Dentro de los tres mas basicos tenemos:
- id
- clase
- elemento

Estos tres corresponden a los atributos que se pueden agregar a cualquier etiqueta dentro de HTML. id="", class="" y el nombre propio de cada etiqueta \<h2\> \<p\>, etc

#### Clases
Para seleccionar una clase se utiliza como primer caracter el \. para marcar que se trata de una clase.
```CSS
.class {

}
```

#### Elemento
Para seleccionar un elemento basta con escribir el nombre de la etiqueta en particular dentro de la hoja de estilos
```CSS
p {

}
```

#### Id
Para seleccionar un ID basta cone scribir como primer caracter \#.
```CSS
#id {

}
```
### Comodin
Existe un comodin especial que sirve para seleccionar todo a lo que nos referimos en determinado contexto. 

El simbolo del comodin especial es \*.
```CSS
* {
	color: red; /* Bajo este contexto estamos seleccionando todo el documento HTML*/
}
```
## Propiedad / Atributo
Es una propeidad que debe ser escrita dentro de un selector y que nos sirve para indicar la propiedad especifica de dicho elemento que va a ser aplicada para el y todos los relacionados a el. Ya sea por selector o por jerarquia dentro de conteenedores

```CSS
h2 {
	color: red; /*Todos los headers H2 tendran la propiedad color en rojo*/
}
```

px es absoluta para cualquier dispositivo sin importar su tamaño.

rem es relativa basada en el tamaño base del font definido en el documento HTML. 

```CSS
html {
	font-size: 10px;
}

h2 {
	font-size: 2rem; /* 20px porque 2 * 10 = 20/
}
```

