---
title: "ApplicationContext"
date: "2022-10-29 15:19"
tags: 
  - spring
draft: false
---
El ApplicationContext es la representacion mas completa del IoC Container, tiene absolutamente toda la funcionalidad basica proveniente del [[notes/BeanFactory]]. 

Este es encargado de instanciar, manejar y construir los objetos llamados "Beans". Asi mismo, este maneja su ciclo de vida, sus scopes y mas cosas de ellos.

Algunas implementaciones concretas de esta interfaz las podemos ver en ClassPathXmlApplicationContext y FileSystemXmlApplicationContext las cuales son mayormente utilizadas en aplicaciones solas. 

Tambien podemos ver la implementacion WebApplicationContext utilizada en contextos Web.
