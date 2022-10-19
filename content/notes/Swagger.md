---
title: "Swagger"
date: "2022-10-08 19:23"
tags: 
  - programming
draft: fakse
---
Es un conjunto de aplicaciones que sirven para generar codigo y documentacion interactiva siguiendo el estandar de OpenAPI.

## Integracion en Spring
En Spring puede ser integrada para hacer ingenieria inversa, es decir, generar un documento Swagger a partir de una API ya establecida. Para ello existe una libreria llamada springfox

La libreria nos añade anotaciones para poder documentar la interfaz generada de Swagger.
- @ApiModel - Documentacion para el modelo
- @ApiModelProperty - Documentacion para un atributo del modelo
- @Api - Documentacion para un controlador
- @ApiOperation - Documentacion para un metodo de un controlador
- @ApiResponse - Documentacion para un metodo de un controlador, pero especifico para los codigos de respuesta
- @ApiParam - Documentacion para los parametros de un metodo


Ademas, es buena practica guardar el YAML que te da esta ingenieria inversa como documentacion para referencias futuras.

## Referencias
[Curso de microservicios con Java y Spring Boot](reference/@%20Curso%20de%20microservicios%20con%20Java%20y%20Spring%20Boot.md)