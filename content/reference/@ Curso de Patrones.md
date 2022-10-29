---
title: "Curso de Patrones"
date: "2022-10-20 08:51"
tags: 
  - 
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
Hacer YAGNI en tu vida es ansiedad, te inventas problemas, miedos y cosas que te incomodan sin que siquiera pasen. Lo mismo en el Software, no te vayas inventando problemas por que te vas a quemar.
- strategy = inyeccion de dependencias = relaciones de asociacion

Todas las listas de antipatrones, patrones, etc se reducen a Cohesion, Acoplamiento y Tamaño.

Normalmente la herencia no se aplica porque si, sino porque representa un punto critico de la aplicacion que es muy extensible

###### ¿Qué es un patron de Diseño?
***Una solucion para un problema en un contexto.***
- Solucion = Conjunto de Objetos y Clases
- Problema = Problema de Diseño (mantenibilidad, reusabilidad, flexibilidad, legibilidad, etc)
- Contexto = Dominio del software

###### ¿Qué nos llevo a utilizar patrones?
Los expertos reconocen que hacer diseño y rediseño (mantener la cohesion, el acoplamiento y el tamaño) es dificil.

Conocerlos, sirve como una caja de herramientas la cual podemos utilizar para resolver los problemas de diseño.
**Utilizamos Patrones por incumplir algun principio de diseño (anti patron, smell code)**
###### ¿Qué se espera conseguir de un Patron?
- Ahorrar tiempo
- Reusar tecnicas ya probadas que vuelven a un sistema mantenible
- Integrarte a la comunidad de desarrollo profesional mediante la expancion del conocimiento
- Expandir tus horizontes para hacer un mejor diseño

###### ¿Cuáles son los elementos de un patron?
- Nombre. Identificador del Patron que puede referirse al problema + solucion.
- Problema. Especifica cuando aplicar el Patron.
	- Motivacion: Problema y Como resolverlo. (Cual y Como)
	- Intencion: Razon de ser y que hace el patron. (Por que y que)
	- Aplicabilidad Condiciones bajo las cuales se debe aplicar. (Cuando)
- Solucion. Describe los elementos del diseño incluida sus relaciones, colaboraciones y responsabilidades que sirven para solucionar el problema.
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

Prototipo y Abstract Factory son similares

Singleton Acceso global a una unica isntancia desde un unic punto

Factory Method Utilizar un colaborador u otro dependiendo de un tipo (sencillo) Basda en Herencia y Estatica

AF. Familias de objetos que deben cambiar de modo dinamico

Builder Reducir complejidad de creacion

Prototype El hermano de Abstract Factory

## Patron Builder
El problema conocido es cuando *Una persona desea comer distintas saludable, para ello necesita variar mucho sus comidas. Sin embargo, hay dias que quiere disfrutar y hay dias que quiere comer comida no tan saludable.*.

Aqui ya vemos el punto de extension. Un if  (en este caso, con solo dos casos) que tiene tendencia a incrementar.

En el problema sin aplicar el Builder la Persona debe conocer a todos y cada uno de los Platos y tiene un metodo largisimo con un switch que depende ciertas circunstancias come saludable o sano o un punto intermedio o mas sano que saludable, etc etc.

Aplicando un Builder se introduce a un "Chef" intermedio (abstract) del cual subyacen todos los tipos de Chef que preparan las comidas para las distintas situaciones que quiere la Persona. 

La Persona no conoce ningun Plato. Conoce a los Chefs que preparan platos, cada tipo de chef conoce los platos que le competen.

Builder es muy complejo porque una cosa tiene muchas otras de forma interna y se le tienen que colocar todos.

Abstract Factory no es complejo crear las cosas, lo complejo son conjuntos enteros d eelementos que es lo que hace complejo

## Patron Factory Method
El problema conocido es cuando *Un Repartidor puede usar mutliples vehiculos para transportarse, dependiendo lo disponible este seleccionara uno u otro*.

La complejidad viene de que el Repartidor se tiene que esforzar en repartir y en ver la disponibilidad de los vehiculos e instanciarlos.

La forma de Solucionarlo es volver a Repartidor abstracta con el metodo que le de un vehiculo y cada uno de los repatidores sabra que vehiculo instanciar. 

Se dice que es estatico porque un RepartidorEnBicicleta esta acoplado para siempre con una Bicicleta y no puede cambiarse de forma dinamica.

## Patron Prototype 
Es el hermano del Abstract Factory. Traido desde el mundo dinamico (js) hacia el estatico.

Con Abstract Factory se satisfacen familias de objetos. Con el prototype lo mismo.















































