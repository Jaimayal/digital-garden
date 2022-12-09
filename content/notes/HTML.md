---
title: "HTML"
date: "2022-12-07 16:16"
tags: 
  - programming
draft: true
---
Es un lenguaje de marcado que sirve para construir sitios web. Este se encarga de definir la estructura literal para un sitio web. 

Adicionalmente tambien permite incluir organizar estilos, codigo y toda la estructura de una pagina.

Finalmente, tambien incluye metainformacion que sirve para expresar informacion hacia otras computadoras como SEO o herramientas de accesibilidad.

El punto de entrada para cualquier sitio es un index.html. Esta es la pagina por defecto que se lee para cargar la pagina inicial.

## Elementos
Existen tres elementos principales que existen dentro de HTML.
- Etiquetas (Tags)
- Atributos (Attribute)
- Contenido (Content)

Dentro de los atributos existen ciertos tipos especiales que son especificos para una etiqueta y que son necesarios para proveer la funcionalidad de la etiqueta de HTML.

```HTML
<tag attribute="value" id="atributo">
	CONTENT
</tag>
```

## Boilerplate
Existe un boilerplate necesario para que el navegador pueda interpretar de forma adecuada un archivo html

### Etiqueta HTML
Marca que el contenido que se encuentra dentro de el es verdadero HTML

### Etiqueta Head
Marca contenido extra en forma de metadatos que sirve para guardar informacion extra para SEO, el set de caracteres, el tamaño a tomar bajo diferentes dispositivos entre otros.

Algunos elementos de meta informacion importante son:
- Title. 
- meta charset
- meta description
- meta keywords
- meta viewport
### Etiqueta Body
Marca el inicio del cuerpo de la pagina. Lo que se carga en ella. No mas metadatos, solo etiquetas que representan informacion


## Headers & Paragraphs
Existen seis niveles de Headers que cambian el tamaño, la fuente y la forma en que los motores de busqueda leen tu pagina.
- H1 el header mas importante y prominente. 

Un paragrafo guarda informacion

Cada una de estas etiquetas guarda sus propios estilos, fuentes, tamaños, margenes y todo.

Existen dos formas para meter un salto de linea:
- Escribir dentro de una nueva etiqueta de paragrafo
- Escribir una etiqueta \<br\>

Adicionalmente existen etiquetas especiales que sirven para enfatizar texto. \<strong\> y \<em\> ambas se utilizan cuando el contenido que tienen tiene un significado fuerte o distintivo de lo que los rodea.

## Contenedores
Utilizados  para agrupar secciones juntas.
- div. Division, un bloque distinto para separar del resto de contenido. No hace ningun cambio en la pagina, solo sirve para agrupar y brindar facilidades para colocar estilos. Es un contenedor de display-block, con lo que despues de este y antes de este se incluira un salto de linea.
- span. Sirve para agrupar tambien en una pagina, sin embargo, es un contenedor que display-inline, significa que sigue dentro de la misma linea y no crea un salto de linea.


No tienen significado semantico. Unicamente son separadores. 

## Lists
Existen dos tipos de listas. 
- Ordenadas ol
- Desordenadas ul

Estas solo son contenedores para las listas, cada uno de los elementos de una lista debe estar contenido dentro de su propia etiqueta \<li\>.

Pueden encontrarse anidadas entre ellas.

## Botones
Los botones son marcados con la etiqueta \<button\> y sirven para marcarun boton al que posteriormente se le puede agregar funcionalidad

Atributos importantes
- disabled
- type. define un tipo de boton. un ejemplo es "submit"

## Boolean Atributos
Son atributos especiales los cuales solo pueden tener valores de verdadero o falso, pero no es necesario que se incluyan entre ellos, con solo incluir su nombre se coloca su valor a true.

Un ejemplo de un atributo booleano es disabled de un boton

## Anchor Tags (Links)
Un link es un anchor tag.  \<a href="url.com"\>. Mediante esta podemos agregar links a otros sitios, tambien llamado hipervinculo.

Adicionalmente podemos agregar cualquier cosa dentro de un anchor tag y convertirlo en un link. Puede ser un \<button\> o un \<img\>.

Un atributo especial es target. Utilizandolo podemos hacer que se abran nuevas pestañas o se abra en la pestaña actual al clickear el link dentro de este

## Imagenes
Para agregar imagenes a un sitio tenemos la tag \<img\> que nos ayuda a agregar una imagen. Para agregarla debemos linkearla como un asset utilizando el atributo src.

El atributo alt es una descripcion de la imagen que sirve como reemplazo para cuando la imagen no se puede mostrar y sirve como accesibilidad para personas discapacitadas.

## Formularios
Son utilizados para cuando el usuario debe insertar informacion para comunicarse con el sitio web. Para subir informacion necesitamos apoyarnos de un boton o de un input con el atributo tipe="submit".

### form
La etiqueta inicial de todo formulario es \<form\>.

Un atributo escencial de este es action, en este atributo definimos una URL a la cual se dirigiran los datos a traves del metodo POST para que el sitio que la recibe trabaje con ella.

atributo method.
### input
Es una etiqueta que sirve para marcar un area de entrada con la que el usuario interactua para llenar de informacion. 

Podemos definir un tipo especifico asignandolo en el atributo type.
- password
- email
- text

atributo name. Sirve para darle un identificador unico como llave para acceder a los valores que se envian por el formulario.
### textarea
Es una etiqueta que sirve como un area de texto en la cual el usuario puede insertar texto largo de multiples lineas. La mejor practica es utilizarlo. Ademas, cuenta con atributos como cols y rows que sirven para cambiar su longitud y la cantidad de texto que se guarda en el.

### label
Sirven para marcar un input y darle una identidad. Estos deben estar linkeados hacia los inputs asignandolos en el atributo especial for="". En el label se debe de matchear el id unico que identifica al input type.

### select
Crea un selector en el cual puedes establecer multiples opciones. la etiqueta inicial es \<select\> y dentro de ella se coloca una serie de opciones cada una con su respectiva etiqueta \;option}:

```HTML
<form method="POST" action="index.html">
	<select name="colors" id="colors">
		<option value="red">Red</option>
		<option value="blue">Blue</option>
	</select>
</form>
```

Adicionalmente tambien podemos crear un label especifico para un select!

### input checkbox
Es un tipo de input que cuenta con un checkbox el cual solo tomara un valor booleano de on or off en el cual el key sera el valor de cada uno de los input bajo el atributo name.

### input radio
Es un tipo de input multiopcinal en el cual de un grupo de opciones se permite solo seleccionar una en un boton con forma de circulo.

## Estilos y Scripts
- En linea
- Bloques
- Importados

### En Linea
#### Estilos
Son estilos en linea que utilizan el atributo especial "style" dentro de cualquier etiqueta. No es muy recomendado utilizarlos debido a que tu estructura se mezcla con estilos y muchas veces es dificil identificar donde se encuentra.

Otra cosa a tener en cuenta esque el estilo en linea siempre tendra prioridad sobre la declaracion de estilos utilizando otros medios

#### Scripts
Los scripts se declaran de forma similar que el CSS, en este caso, se utilizan atributos especiales para los eventos como "onclick". SIn embargo, estos tienen los mismos inconveniente que utilizar estilos en linea.

### Bloques
#### Estilos
La etiqueta \<style\> sirve tambien para marcar un bloque de texto en el cual podemos insertar un bloque muy grande de CSS sin problemas hasta que cierre el bloque.

#### Scripts
Una etiqueta equivalente tambien existe al insertar un script de JS. Para ello, se utiliza la etiqueta especial \<script\>. Dentro de esta se escribe la cantidad de codigo de JS que sea necesaria


### Importados
#### Estilos
Los estilos se importan de forma especial en forma de metadatos en el header del archivo de HTML.

Para hacerlo, debe de existir un archivo aparte que contenga todos los estilos, estos deben de llevar la terminacion .css.

Estos se importan utilizando la etiqueta \<link\> con el atributo rel especificando que se trata de un stylesheet y un href para referirse a la localizacion de la hoja de estilos.

#### Scripts
Los scripts se importan de la misma forma que los estilos, pero esta vez se utiliza la etiqueta \<script\> con su atributo especial src para marcar la localizacion del archivo

## Elementos Semanticos vs Estructurales
Inicialmente tenemos elementos estructurales como \<div\> y \<span\> que nos sirven para agrupar contenido, como ya sabemos.

Sin embargo, tambien existen otro tipo de elementos llamados semanticos dentro de los cuales podemos declarar contenido y otras etiquetas. Proveen muchas veces la misma funcionalidad que los contenedores estructurales pero estos nos ayudan a entender un poco mejor el codigo HTML que estamos trabajando.

## Data tag
Es una forma de guardar un valor que es transparente para los usuarios pero que puede ser usado a futuro en un script para guardar un estado que se busca que tenga un contenedor o lo que sea.

## iFrame
Es una forma de linkearse y visualizar otros sitios para su uso dentro de tu pagina. Mediante este se puede tener una pagina web dentro de una pagina web.