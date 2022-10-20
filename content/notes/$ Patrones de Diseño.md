---
title: "$ Patrones de Diseño"
date: "2022-10-20 08:52"
tags: 
  - pattern
  - gof
draft: true
---
Hacer YAGNI en tu vida es ansiedad, te inventas problemas, miedos y cosas que te incomodan sin que siquiera pasen. Lo mismo en el Software, no te vayas inventando problemas porque te vas a quemar.
- strategy = inyeccion de dependencias = relaciones de asociacion

- A un problema recurrente una solucion reusable cambiando los detalles minimos.

###### ¿Por qué utilizar patrones?
- Ahorra tiempo
- Reusa tecnicas ya probadas infinitamente
- Te integra a una comunidad
- Expande tu conocimiento

###### ¿Cuáles son los elementos de un patron?
- Nombre. Identificador del Patron
- Problema. Lo que resuelve.
	- Motivacion: Problema y Como resolverlo. (Cual y Como)
	- Intencion: Razon de ser y que hace el patron. (Por que y que)
	- Aplicabilidad Condiciones bajo las cuales se debe aplicar. (Cuando)
- Solucion. Como lo resuelve
- Consecuencias. Compromiso por aplicarlo

## Patron Singleton
- **Nombre**: Singleton
- **Problema**. 
	- Motivacion: Para algunas clases es importante compartir una unica instancia en el sistema. 
	- Intencion: Asegurar que una clase tenga una unica instancia y proveer un punto de acceso global a ella.

