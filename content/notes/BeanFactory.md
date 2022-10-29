---
title: "BeanFactory"
date: "2022-10-29 15:19"
tags: 
  - spring
draft: true
---
BeanFactory es la representacion mas basica del IoC Container en Spring.

Este tiene funciones simples las cuales hereda hacia el [[notes/ApplicationContext]]. 

Una de las propiedades principales de este contenedor esque tiene una inicializacion *Lazy*, es decir, que no va a cargar los beans hasta que se llame a su metodo .getBean(String name).

Por otro lado, unicamente cuenta con dos tipos de Scope que le puede dar a los beans:
- Singleton
- Prototype

Debido a su inicializacion *Lazy*, este contenedor es considerado muchisimo mas ligero para desarrollar una aplicacion. Por tanto, debe ser usado cuando el consumo de memoria es critico para el desarrollo de una aplicacion.
