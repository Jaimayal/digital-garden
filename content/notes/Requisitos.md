---
title: "Requisitos"
date: "2022-09-03 08:56"
tags: 
  - softwaredev
draft: false
---
Es uno de los primeros procesos en el [Desarrollo de Software](notes/Desarrollo%20de%20Software.md). Ocurre cuando se establece comunicacion entre los [Stakeholders](notes/Stakeholders.md) y el equipo de desarrollo. 

Su objetivo principal es convertir las necesidades de los clientes en requisitos claros que puedan ser interpretados por el equipo de desarrolladores. Por tanto, es necesario tener un buen conocimiento del [Dominio de Negocio](notes/Dominio%20de%20Negocio.md) de la empresa que busca el Software.

Para realizarlo se utiliza distintas practicas, incluso traidas de la ingenieria (muchas de ellas traidas de *requirements engineering*),

En caso de no tenerlos se puede incurrir en saber que es lo que se tiene que hacer pero fallar al proponer las soluciones posibles para lograrlo.

![[files/RequisitosFallo.png]]

## Lidiar con Cambios en los Requisitos
1. Hacer que todos entiendan los costos en los que se incurre. Tanto de tiempo como de dinero.
2. Establecer un plan de control para satisfacer las demandas de cambios. Los desarrolladores estaran felices porque sabran cuando llegan nuevos pedidos y los clientes porque se sentiran escuchados.
3. Utilizar metodologias que se adapten bien a los cambios. Usualmente entre las [[notes/Metodologias de Desarrollo]] las que mas son adaptables a cambios son las Iterativas.
4. Mantener en mente la [[notes/Definicion del Problema en un Desarrollo de Software]] para saber si algo es trivial o no

## Tipos
Existen dos tipos inherentes de Requisitos del Software
- Requisitos Funcionales. Lo que debe hacer el Software
- Requisitos No Funcionales. Lo que se espera del Software

Entre ambos e incluso entre requisitos de la misma categoria existen un compromiso constante en el que se deben de balancear y hacer intercambios de una cosa por otra. Puedes reducir la complejidad mientras empeoras la eficiencia, puedes incrementar la reusabilidad mientras empeoras la legibilidad, todo depende de que busques y como lo hagas.

Algunos requisitos no funcionales populares son
- Time to Market
- Mantenibilidad del Codigo
- Reusabilidad
- Extensibilidad
- Legibilidad
- Eficiencia
- Eficacia

En escencia, estos requisitos son los que generan la Complejidad en el Software.
## Referencias
- [[reference/@ Code complete]]
- [[reference/@ The essentials of modern software engineering_ Free the practices from the method prisons!]]