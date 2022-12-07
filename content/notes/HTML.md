---
title: "HTML"
date: "2022-12-07 16:16"
tags: 
  - 
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