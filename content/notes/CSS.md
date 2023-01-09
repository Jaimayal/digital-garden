---
title: "CSS"
date: "2022-12-09 08:06"
tags: 
  - programming
  - css
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

#### Especificidad
Adicionalmente, entre ellos existe una Jerarquia, de modo que, si tenemos una misma etiqueta referida en la hoja de estilos de tres formas diferentes (por su etiqueta, clase e id) se seguira la siguiente jerarquia:
1. ID
2. Clase
3. Selector

Es decir, que en nuestro ejemplo, las propiedades descritas en el bloque del id sobreescribiran las propiedades definidas en su clase y en su selector. Sin embargo, si una propiedad definida en su clase o selector no se encuentra sobreescrita este lo conservara.

Ademas de esto, podemos comprobar si hay una sobreescritura de propiedades en las herramientas de desarrollo de Google.
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

## colores
Una forma de ganar mas control sobre los colores es utilizar cualquiera de estos tres:
- rgb
- rgba
- hexadecimal
- nombre

Una forma de conseguir una paleta de colores es el sitio happyhue que te brinda una paleta de colores para utilizar en tus paginas web.
### texto
Para el texto tenemos la propiedad color

### background
Cambia el color del contenedor y su padding al color especificado

### border
En un borde se puede especificar en la misma linea el color deseado.


## Bordes
Todo dentro de una pagina web se encuentr dentro de contenedores. Una forma de visualizarlo es 

Cada contenedor esta construida de cuatro cosas
- content
- padding
- border
- margin

![[files/BoxModel.png]]

Cada una de estas aporta una cantidad de espacio para separarla de otros elementos y tiene sus respectivas propiedades para ser modificada.

El area de contenido cuenta con propiedades para ser especificada:
- width
- height
- min-width
- min-height
- max-width
- max-height

Usualmente, width y height son especificadas con % para hacer un diseño responsivo. Las otras son marcadas con fijos (como px) para mantener un tamaño fijo sin importar el tamaño del dispositivo.

### Padding y Margin
Estos sirven para crear layouts, spacing y colocar todo. Existen dos diferencias principales entre margin y padding:

Estan divididas por un border intermedio. Es importante tener en cuenta la existencia de este elemento porque marca toda la diferencia entre el comportamiento de ellos, es un delimitador que sirve para marcar donde inicia el contenido y donde termina.

De modo que, Padding se comporta respectivo al contenido interno y Margin respecto al contenido externo.

### Border
Es el separador entre Padding y margin. Dentro de CSS puede ser especificado con la propiedad border. Este tiene tres valores principales bastante unicos.

- tamaño
- tipo
- color

Dentro del tamaño podemos especificar cualquier medida para que tenga como separador, usualmente esta entre los 1 a los 3 pixeles.

Dentro del tipo diferentes estilos para utilizar, tenemos solid, dashed y otros que solo cambian como se ve.

Dentro del color podemos utilizar cualquier forma de CSS para seleccionar color, rgb, rgba, hexadecimal, etc.

## Box-Sizing
Es una propiedad que sirve para definir como interactuan border, padding y content respecto al width definido para el contenido.

Existen dos principales que son utilizados comunmente:
- content-box. Contempla que solo el content tome el width definido sin tomar en consideracion lo demas.
- border-box. Contempla que la suma de borde + padding + content tome el width definido anteriormente.
### Mejores Practicas
- Utilizar porcentajes en el contenido (width y height)
- Utilizar medidas absolutas para el min-width, min-height, max-width y max-height
- Utilizar las medidas especiales vh y vw para margen y padding.

## Selectors Avanzados
### Descendant
El espacio es el selector descendiente. Marca que un selector se debe encontrar forzozamente dentro de otro para que se le apliquen los estilos.

```CSS
.conteenedor .selector {
	/*Todos los elementos dentro de la clase contenedor que tengan la clase selector recibiran las propiedades aqui marcadas*/
}
```

### Padre
Este es un selector que utiliza el caracter especial \>. Marca que se aplicaran las propiedades a el selector del lado derecho del operador siempre y cuando su padre inmediato sea el selector a la izquierda del operador.

```CSS
div > p {
	/*Todos los elementos p donde su padre inmediato sea un div*/
}
```

### Lista
Te permite asignar las mismas propiedades a diferentes selectores a la vez en forma de lista

```CSS
h1, h2, p {
	/*Todas estas propiedades se aplicaran a todos los h1, h2 y p*/
}
```

### Elemento con Clase / Combo
El operador especial es no dejar ningun espacio entre ellos. Sirve para referirte a todos los elementos que tengan la clase especificada.
```CSS
p.class {
	/*Las propiedades se aplicaran a todos los elementos p siempre y cuando tengan la clase especificada*/
}
```


### Adjacente
El operador especial es +. Te permite referirte al selector de la derecha siempre y cuando se encuentre adyacente al de la izquierda. Es decir, que se encuentren en el mismo nivel de anidacion y que al terminar el de la izquierda inmediatamente inicie el de la derecha
```CSS
h1 + h2 {
	/*Todas las propiedades se aplicaran a un H2 siempre y cuando antes de el termine un h1*/
}
```


### Mismo nivel
El operador especial es ~. Te permite referirte al selector de la derecha siempre y cuando se encuentren en el mismo nivel de anidacion, sin importar si son consecuentes o no.

```CSS
h1 ~ p {
	/*Todas estas propiedades se aplicaran a todos los p siempre y cuando esten en el mismo nivel de anidacion que h1*/
}
```

## Pseudoclases
Existen pseudoclases en forma de selectores que sirven para referirse a estados que pueden ocurrirle a un selector.

Las pseudoclases utilizan la sintaxis de los : (dos puntos) para referirse a ellas.

Un detalle muy importante a tener en cuenta con ellas esque **una pseudoclase siempre va despues del bloque en el que se definen los estilos para el selector base**

Entre los principales tenemos
- :hover. Aplica estilos cuando el mouse se encuentra sobre el elemento y los remueve cuando se quita el mouse.

```CSS
h1:hover {
	cursor: pointer;
	color: white;
	background-color: darkblue;
	transition: 1s ease all;
}
```

Muchas de las pseudoclases tienen que ver con las interacciones que ha hecho el usuario.
- :focus

Adicionalmente tambien hay otras clases que sirven como selectores y no interaccionan tanto con el usuario. Algunos ejemplos de ellos son:
- :first-child
- :last-child
- :nth-child
- :first-of-type

## Transition
Usualmente utilizada con la pseudoclase hover sirve para insertar la animacion de transicion. Recibe tres propiedades en su forma mas simple, al igual que border:

- tiempo. El tiempo que toma la animacion en ejecutarse
- bizarre. define donde ocurre la aceleracion al ocurrie el evento
- llave atributo. El nombre del atributo a la cual se aplicara la transicion

## Transform
Te ayuda a definir una funcion para transformar tu elemento. Hay muchas de ellas predefinidas y cada una de ellas recibe un valor especifico, muchas veces,  es una medida. 

Dentro de las predefinidas, tenemos una funcion muy importante llamada translate, que sirve para desplazar el elemento una medida definida hacia abajo, derecha, izquierda, etc. 

Todo esto forma parte de las animaciones que le dan un toque mas profesional al sitio.

## Pseudoelementos
Adicionalmente existen pseudoelementos que nos permiten seleccionar elementos y referirnos a otros elementos. Los mas importantes son:
- ::before
- ::after

Estos dos nos permiten seleccionar el elemento antes del selector y despues del selector.

## Background
Ademas de background-color, podemos designar una back-ground image para tener algo de fondo en cualquier contenedor.

```CSS
#container {
	background-image: url('image.png');
	background-size: 100%;
	background-position: bottom;
}
```

Una forma de conseguir imagenes para un fondo es utilizando el sitio [unsplash](https://unsplash.com/photos/).

## Display
Las dos mas comunes utilizadas es inline y block. Todos los elementos (aun si la propiedad no esta definida explicitamente) tienen una. La mayoria de los elementos en HTML tienen por defecto el valor block.

- block rellena el ancho de toda la pagina de forma automatica
- inline el ancho no toma toda la pagina, solamente toma el ancho que tenga el texto por defecto. De modo que se pueden colocar multiples elementos inline y otros elementos con display inline de forma consecutiva.

La desventaja de utilizar elementos inline esque los unicos espacios que puedes manejar son los horizontales. Los verticales por defecto se encuentran desactivados para margin, padding y height.

Una forma de combinar lo mejor de los bloques (conservar padding, height y margin vertical) y de los inline (mantener todo en una misma linea) es el display especial inline-block.

```CSS
a {
	display: inline-block;
	margin: 20px
}
```

## Position
Es una forma de posicionar en el espacio de una pagina distintos contenedores.

### Relative
Marca un contenedor con posicion relativa sobre el cual otros contenedores pueden marcar sus posiciones.


### Static
Es el valor por defecto de todos los elementos. Es estatico en la pagina.

### Absolute
Los valores absolutos seran relativos al primer contenedor que tenga la position en relative. En caso de no tener ninguno, body por defecto adquiere esta propiedad.

### Fixed
Tambien coloca a un contenedor en posicion arreglada que se escapa del comportamiento de otros contenedores.

Para un correcto funcionamiento podemos aprovechar la propiedad z-index para colocar los contenedores que queremos en la jerarquia que queremos dentro de nuestr apagina web para que uno aparezca sobre otros.

Es usualmente utilizado en navs.
## Display Flex - Flexbox
Es uno de los mas populares y formo su propia forma de distribuir elementos en una pagina web. Este display en particular cuenta con sub atributos que permiten modificar el comportamiento del contenedor.

### flex-direction
Cambia la direccion hacia donde se orienta el flex, puede ser en forma de columna o row, inversa o normal. Esto ayuda a dirigir los elementos con una orientacion y hacia el lado que queramos


### flex-wrap
Te ayuda a definir mas comportamientos, esta vez relacionados con la responsabilidad y el tamaño de un elemento. En caso de que los elementos de un contenedor excedan el tamaño que tiene la aplicacion esta los pasara a una nueva fila manteniendo el tamaño de cada uno.
```CSS
.container {
	display: flex;
	flex-wrap: wrap;
}
```


### justify-content
Te ayuda a definir el espacio de los elementos del contenedor. Puedes definir espacio entre ellos, centrarlos, separarlos, moverlos al final, entre otros. Este es espacio horizontal

### align-items
Te ayuda a definir los mismos espacios entre elementos pero esta vez trabaja con el espacio vertical.

### align-self
Permite alinear un solo elemento del contenedor en el eje vertical

### flex-grow
Te permite cambiar el tamaño de todos los elementos para rellenar el contenedor padre. Esto trae un problema con el flex-wrap debido a que no hay un minimo tamaño a partir del cual se deba usar el wrap. Para ello existe otra propiedad llamada flex-basis

### flex-basis
Sirve para definir un tamaño minimo a partir del cual la propeidad flex-wrap debe actuar.

### flex'shrink
Sirve para mantener el tamaño de un elemento sin importar los otros elementos al cambiar de tamaño.

## Media Queries
Te permite hacer que tu sitio se mire aplicando diferentes estilos dependiendo el tamaño de la pantalla en la que quieres visualizar. Tiene una sintaxis especial utilizando el @ como caracter especial. 

```CSS
@media only screen and (max-width: 500px) {
	.container {
		color: red;
	}
}
```

La forma mas comun de escribir el CSS es escribir primero el contenido para movil primero. 




