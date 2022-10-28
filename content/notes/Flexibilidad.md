---
title: "Flexibilidad"
date: "2022-10-28 17:56"
tags: 
  - oop
draft: true
---
## Clases Abstractas e Interfaces
La interfaz es un contrato que existe entre una clase derivada y la interfaz, declara que, toda clase que la implemente como minimo debe implementar de forma concreta un algoritmo para los metodos si no quiere ser abstracta.

Una interfaz es una clase abstracta pura la cual no fomenta la reusabilidad porque no tiene atributos ni metodos que debe transmitir, solo cabeceras de metodos (es decir, solo la interfaz).

Por otro lado, las interfaces aportan mucha flexibilidad con respecto al cambio, porque, mientras que una clase concreta implemente esos metodos a nadie le interesa que tecnologias utiliza o como lo este haciendo.

## Herencia vs Delegacion
Como sabemos, la herencia permite transmitir metodos y datos de una clase base a unas clases derivadas. Asi mismo, si es una clase abstracta permite tener implementaciones entre meditas y utilizar el Template Pattern.

Sin embargo, todo esto tambien es posible hacer mediante una Composicion utilizando el mecanismo de Delegacion.

Con el mecanismo de Delegacion, una clase todo puede utilizar el codigo de su parte para brindar un servicio, esta clase todo tiene un nivel de abstraccion debido a que los clientes que interactuan con el no saben ni la existencia de sus partes.

Mediante la delegacion tambien podemos aplicar el Template Pattern, teniendo en la clase parte una llamada al metodo de la clase Todo.

Esto forma un ciclo, debido a que la clase todo conoce a la parte y la parte al todo para llevar a cabo el Template Pattern.

La forma de romperlo es meter una interfaz, de modo que la Parte puede utilizar a cualquiera que implemente la interfaz con el metodo que se encuentra dentro del Template y no necesita conocer de forma directa a ningun Todo.
