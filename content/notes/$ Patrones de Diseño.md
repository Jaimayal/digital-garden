---
title: "$ Patrones de Diseño"
date: "2022-10-20 08:52"
tags: 
  - designpattern
draft: true
---
Hacer YAGNI en tu vida es ansiedad, te inventas problemas, miedos y cosas que te incomodan sin que siquiera pasen. Lo mismo en el Software, no te vayas inventando problemas porque te vas a quemar.
- strategy = inyeccion de dependencias = relaciones de asociacion

Todas las listas de antipatrones, patrones, etc se reducen a Cohesion, Acoplamiento y Tamaño.

Normalmente la herencia no se aplica porque si, sino porque representa un punto critico de la aplicacion que es muy extensible

###### ¿Qué es un patron de Diseño?
- A un problema recurrente una solucion reusable cambiando los detalles minimos.

###### ¿Qué nos llevo a utilizar patrones?
Los expertos reconocen que hacer diseño y rediseño (mantener la cohesion, el acoplamiento y el tamaño) es dificil.

Conocerlos, sirve como una caja de herramientas la cual podemos utilizar para resolver los problemas de diseño.

###### ¿Qué se espera conseguir de un Patron?
- Ahorrar tiempo
- Reusar tecnicas ya probadas
- Integrarte a la comunidad de desarrollo profesional mediante la expancion del conocimiento
- Expandir tus horizontes para hacer un mejor diseño

###### ¿Cuáles son los elementos de un patron?
- Nombre. Identificador del Patron
- Problema. Lo que resuelve.
	- Motivacion: Problema y Como resolverlo. (Cual y Como)
	- Intencion: Razon de ser y que hace el patron. (Por que y que)
	- Aplicabilidad Condiciones bajo las cuales se debe aplicar. (Cuando)
- Solucion. Como lo resuelve
- Consecuencias. Compromiso por aplicarlo

###### ¿Cuál es la intencion del Patron Singleton?
*Asegurar que una clase tenga una unica instancia y proveer un punto de acceso global para esta*.

###### Cohesion
La cohesion es el resultado del Reparto de Responsabilidades. Hacerlo bien dara una buena cohesion, hacerlo mal, causara lo contrario-

###### ¿Qué variaciones se le pueden agregar al Patron Singleton?
- Herencia (Cumplir Open-Closed)
- Multiples instancias (Como un pool)

###### ¿Cuáles son las clasificaciones de los Patrones de Diseño?
Son tres clasificaciones
- Patrones Creaciones
- Patrones Estructurales
- Patrones de Comportamiento

###### ¿Cuáles son los 
- Ocultar una Jerarquia de Herencia mediante el uso de un patron creacional.
- Distribuye la responsabilidad de crear una clase en especifica de modo que permita extenderse de forma ilimitada
- 

###### ¿Cuáles son los tipos de Patrones Creacionales?
- Abstract Factory. Complejidad Grande. N cosas
- Builder. Uno solo es muy complejo de construir
- Factory Method. Complejidad Pequeña. 1 Cosa
- Prototype. Abstract Factory utilizado en lenguajes dinamicos
- Singleton. *Asegurar que una clase tiene una unica instancia y un unico punto de acceso global*.

## Abstract Factory
Es como cuando un cirugano necesita de instrumentos para poder realizar su cirugia. Sin este patron, el cirugano deberia encargarse de instanciar los instrumentos por si mismo. 

Dado caso que se pudieran utilizar diferentes instrumentos basado en un contexto la clase Cirugano adquiriria una cantidad de complejidad extrema.

Aplicando este patron correctamente es como si el cirugano ganara un instrumentalista que le pasara los instrumentos que fueran necesarios cuando sea. Por tanto:
- El cirugano solo tendria que centrarte en la cirugia sin los detalles que no le interesan por tanto, se vuelve mas cohesivo.
- Debido a que ya no se preocupa por los detalles, se desacopla de todos los instrumentos
- Reduce el tamaño de sus metodos de cirugia porque ya no debe encargarse de traer sus instrumentos

### Problema
Un if o un switch en el cual un objeto debe de encargarse de manejar multiples instancias de multiples clases que no tienen nada que ver con su funcion principal.

*Un cirugano que aparte de hacer la operacion, debe traer sus propios instrumentos (akgi cortante y algo para secar) basado en el contexto en el que este (jungla, quirofano, ciudad, etc)*

Proporcionar una interfaz para crear familias de objetos relacionados o dependientes entre si sin tener que especificar su clase concreta































