---
title: "Analisis y Diseño"
date: "2022-09-03 08:51"
tags: 
  - softwaredev
draft: false
---
## ¿Qué es el Diseño?
Es un proceso que se realiza en el [Desarrollo de Software](notes/Desarrollo%20de%20Software.md), su objetivo principal es reducir la complejidad de un software.

## ¿Por qué deberiamos hacer Diseño?
Debido a que se busca realizar un software de calidad para cumplir con todos los aspectos de un proyecto de software.
- Cumplir con los requisitos (el ambito) en tiempo, cumpliendo el coste establecido.
- Con una implementacion efectiva
- Con un codigo bien legible

Nos ayuda a crear codigo de calidad en todos los aspectos (seguridad, legibilidad, mantenibilidad).
- Que se puede probar
- Que se puede leer
- Que se puede evolucionar
- Que se puede reutilizar

Es decir, en rasgos generales, **se busca reducir la complejidad del software**. Como sabemos, la complejidad del software incrementa debido al constante cambio en los [Requisitos](notes/Requisitos.md) y otros problemas.

Popularmente las personas usan el termino *Diseño* para referirse a las dos disciplinas (Analisis y Diseño), pero realmente, estas son dos muy diferentes.
## Analisis
Busca simplificar los requisitos y establecer unos diagramas bases ya hablando en el lenguaje de los desarrolladores. Se enfoca en partir el problema y prepara para tener un buen diseño.

Tambien se establece la terminologia con la que todos van a trabajar para que haya buena comunicacion entre los desarrolladores.

Resultados de esta disciplina:
- Requisitos iniciales formalizados ya simplificados y consisos.
- Diagrama que representa el esqueleto del software a realizar.

> *Para realizar el analisis se tiene que tener un pie en el modelo del dominio*

## Diseño
Busca diseñar en software lo ya analizado y hablar sobre las tecnologias con las que se va a trabajar para desarrollar el proyecto (sistemas operativos, bases de datos, frameworks, lenguajes, etc.). Las transacciones, los metodos, las conexiones, interfaces, etc.

> *Para realizar el diseño se toma en cuenta la implementacion, los frameworks, las tecnologias, etc.*

Resultado:
- Diagramas que ayuden a interpretar las fases iniciales del software.
- Reparto de Modulos y responsabilidades a multiples miembros de un equipo.
- Asignacion de relaciones y vias de comunicacion entre clases. Colaboracion

## Tradeoffs
Al realizar diseño, se deben de tener en cuenta los intercambios que se hacen en las distintas cualidades de un software. Especialmente relacionado a los Requisitos no Funcionales, puesto que se intuye que los requisitos funcionales son garantizados por cumplirse.

Sin embargo, los requisitos no funcionales son mucho mas complejos que ello. Algunos de los aspecots que engloban
- Time to Market
- Mantenibilidad del Codigo
- Eficiencia
- Eficacia

El Analisis y Diseño es un constante balance entre los requisitos no funcionales y funcionales. No se puede tener mucho de unos ni mucho de otros.

## ¿Cómo lograr tener un buen diseño?
Para lograrlo debemos seguir los tres aspectos relacionados con el diseño:
- [Diseño en Codigo](notes/Dise%C3%B1o%20en%20Codigo.md)
- [Diseño Modular](notes/Diseño%20Modular.md)
- [Diseño orientado a Objetos](notes/Diseño%20orientado%20a%20Objetos.md)