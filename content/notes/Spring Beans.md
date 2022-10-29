---
title: "Java Beans"
date: "2022-10-29 15:21"
tags: 
  - java
draft: true
---
Son uno de los conceptos principales que subyacen en el [[notes/Spring Framework]]. En palabras simples son los objetos que forman las partes clave de tu aplicacion, los cuales esperan ser instanciados, construidos y manejados por el contenedor de Spring que tiene la [[notes/Inversion de Control]].

### Creacion
Hay dos formas principales en las cuales podemos crear un bean, la primera y la mas usada es mediante metodos en una clase de @Configuration.

Entendamos primero que, utilizar la anotacion @Configuration en una clase nos garantiza que el contenedor reconocera y ejecutara los metodos que esten marcados con @Bean porque sabe que ahi encontrara algunos debido a que forma parte de la configuracion de la aplicacion.

Posteriormente, notemos que la anotacion @ComponentScan es suplida con un
