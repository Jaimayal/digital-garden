---
title: "Patron Abstract Factory"
date: "2022-10-20 19:00"
tags: 
  - designpattern
draft: true
---
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