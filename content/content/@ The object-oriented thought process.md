---
title: "The object-oriented thought process"
authors: "Matt Weisfeld"
year: 2019
URL: "www.amazon.com/Object-Oriented-Thought-Process-Developers-Library-dp-0135181968/dp/0135181968"
tags: programming oop
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
## Introduction to Object-Oriented Concepts
## How to Think in Terms of Objects
## More Object-Oriented Concepts
Los dos capitulos anteriores sentaron las bases con los conocimientos basicos relacionados a la programacion orientada a objetos. Sin embargo, si lo que se busca es analizar, diseñar y desarrollar un sistema orientado a objetos aun se necesitan ver unos conceptos mas como constructores, herencia multiple, scope, error handling, scope, etc.

### Constructors
Son metodos especiales que son llamados en el momento en el que se busca instanciar un nuevo objeto, sirven para inicializar los valores de los atributos de un objeto.

La sintaxis varia entre lenguajes, algunos utilizan *new*, otros *init*, etc. 

Para el contexto de Java un constructor es como un metodo que debe de llevar el mismo nombre de la clase actual y no debe tener valor de retorno.
#### When is a Constructor Called ?
El constructor es llamado de forma automatica tras instanciar (alocar memoria suficiente para) un objeto de una clase especifica, en Java se utiliza el keyword *new* seguido del nombre del metodo constructor.

#### What's Inside a Constructor ?
El constructor debe contener el codigo suficiente para que los atributos que va a guardar el nuevo objeto tenga un estado limpio y estable.

#### The Default Constructor
Hay un estandar respecto a la creacion de constructores, principalmente debido a que una clase necesita uno obligatoriamente para funcionar, los lenguajes de programacion proveen uno estendar en caso de que ninguno este disponible. Es importante no recaer mucho en este mecanismo y SIEMPRE implementar al menos uno.

En Java por ejemplo, debido a que todos los objetos heredan de la clase Object, podemos saber con exactitud que el constructor default llama al constructor de Object.

Es buena practica implementar AL MENOS un constructor por nosotros mismos para saber que la clase se va a comportar de forma esperada bajo cualquier cambio. 

#### Using Multiple Constructors
Es un proceso que debe ser ejecutado cuando lo que se busca esque distintos objetos de la misma clase sean inicializados o tengan valores diferentes al momento de creacion. 

Para realizar este mecanismo se aprovecha del **method overloading**, que funciona para sobrecargar metodos cambiando la signatura de ellos (tipo, nombre de parametros, cantidad, etc.)

#### Overloading Methods
Es un concepto de programacion en la cual se permite tener metodos multiples metodos de caracteristicas similares siempre y cuando se cambie su signatura.

La signatura de un metodo varia de lenguaje en lenguaje, para Java y C# la signatura consiste del nombre del metodo + sus parametros.

Otros lenguajes consideran al tipo de valor de retorno tambien como parte de la signatura.

Esto es muy utilizado en los constructores, se puede tener sobrecarga de constructores y por tanto, construir un objeto de una misma clase de distintas formas diferentes.
___

