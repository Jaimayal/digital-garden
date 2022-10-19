---
title: "Externacionalizacion"
date: "2022-10-08 19:20"
tags: 
  - softwaredev
  - java
draft: false
---
La externalizacionc es un proceso en el cual se pasan las propiedades que son ajenas al codigo a archivos de texto plano que pueden ser importados hacia el codigo y poder ser utilizados de forma dinamica

En Spring la externalizacion se hace a archivos de texto plano con terminacion .properties (app.properties, config.properties, etc).

Para acceder a ellos se utiliza SpEL y regularmente se crean Beans a partir de estas propiedades en texto plano. 

## Referencias
[Curso de microservicios con Java y Spring Boot](reference/@%20Curso%20de%20microservicios%20con%20Java%20y%20Spring%20Boot.md)