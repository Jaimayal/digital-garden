---
title: "Analisis y Diseño"
date: "2022-09-03 08:51"
tags: 
  - softwaredev
draft: false
---
#### ¿Qué es el Diseño?
Es un proceso que se realiza en el [Desarrollo de Software](../Desarrollo%20de%20Software.md), su objetivo principal es reducir la complejidad de un software.

#### ¿Por qué deberiamos hacer Diseño?
Debido a que se busca realizar un software de calidad para cumplir con todos los aspectos de un proyecto de software.
- Cumplir con los requisitos (el ambito) en tiempo, cumpliendo el coste establecido.
- Con una implementacion efectiva
- Con un codigo bien legible

Nos ayuda a crear codigo de calidad en todos los aspectos (seguridad, legibilidad, mantenibilidad).
- Que se puede probar
- Que se puede leer
- Que se puede evolucionar
- Que se puede reutilizar

Es decir, en rasgos generales, **se busca reducir la complejidad del software**. Como sabemos, la complejidad del software incrementa debido al constante cambio en los [Requisitos](Requisitos.md) y debido a que no se siguen con ninguno de los niveles del diseño:
- [[notes/Diseño en Codigo]]
- [[notes/Diseño Modular]]
- [[notes/Diseño orientado a Objetos]]

Popularmente las personas usan el termino *Diseño* para referirse a las dos disciplinas (Analisis y Diseño), pero realmente, estas son dos muy diferentes.
#### Analisis
Busca simplificar los requisitos y establecer una terminologia en la que todos (expertos, jefes, y desarrolladores) se puedan entender. Esto prepara para tener un buen diseño debido a que se establece la terminologia con la que todos van a trabajar y los criterios a cumplir.

Resultados de esta disciplina:
- Requisitos iniciales formalizados ya simplificados y consisos.
- Diagrama que representa el esqueleto del software a realizar.
- Lista de vocabulario comun para todos los implicados en el proyecto.

> *Para realizar el analisis se tiene que tener un pie en el modelo del dominio*

#### Diseño
Busca diseñar en software lo ya analizado y hablar sobre las tecnologias con las que se va a trabajar para desarrollar el proyecto (sistemas operativos, bases de datos, frameworks, lenguajes, etc.).

> *Para realizar el diseño se toma en cuenta la implementacion, los frameworks, las tecnologias, etc.*

Resultado:
- Diagramas que ayuden a interpretar las fases iniciales del software.
- Reparto de Modulos y responsabilidades a multiples miembros de un equipo.