---
title: "Curso de microservicios con Java y Spring Boot"
date: "2022-10-07 07:43"
tags: 
  - 
draft: true
---
## 🌱 Idea Principal

## 🌌 Impacto

## ✍ Mejores Frases

## 📔 Resumen + Notas
1. Arquitectura Orientada a Microservicios
2. Integracion y Despliegue continuo
3. Java 
4. Spring Boot
5. API REST CRUD
6. Postman Consumo
7. Lombok
8. Externalizacion de Parametros

## Arquitectura Orientada a Microservicios
Monolitico. Software que contiene toda la solucion integra.

Causa dependencias entre cada modulo.

Microservicios. 
- Dividir toda la solucion en multiples modulos llamados microservicios en el que cada uno resuelve una funcionalidad.
- Los microservicios se comunican regularmente mediante REST o sistemas de mensajeria como RabbitMQ.
- Se logra muy bajo acoplamiento afernte y eferente.
- Aumenta la complejidad de despliegue{
- Desarrollo puede ser agnostico al lenguaje
- Permite reutilizarse en distintas soluciones para problemas.

Anatomia de un Microservicio
![[files/ComponentesMicroservicio.png]]

La capa Controller solo debe encargarse de enviar los datos que recibe del mundo exterior a la capa Service.

La capa Service debe contener toda la logica de negocio.

La capa DAO unicamente debe encargarse de comunicarse con la persistencia de la aplicacion

## CI/CD
Docker. Te permite crear un contenedor en el cual puede existir cada microservicio con su sistema operativo. 
- Cada contenedor puede heredar de una imagen base que ya tiene instalada todas las dependencias necesarias para que los microservicios corran

OpenShift. Es un orquestador de maquinas Docker (PaaS) que te permite desplegar cada container de acuerdo a las necesidades que tiene cada uno (load balancing)., es decir, te permite escalar cada microservicio de acuerdo a las necesidades que se tienen.

Spring Specification sirve para meter filtros a los recursos de forma estandarizada.

Una buena practica esque en post se devuelva la ruta donde se puede recuperar el usuario creado.

Otra buena practica es retornar el header Location despues de crear un recurso.

Los controladores normales no deberian de tener recursos anidados, para ellos se debe de crear otro aparte y a su vez para los recursos anidados se debe hacer otro por si se necesitan hacer operaciones mas alla de lectura (CRUD).

Dependiendo del Dominio un JSON deberia o no contener lo relacionado con un recurso y sus anidaciones. Si se requiere, se pueden enviar links para poder recuperar mas informacion del usuario.
## Rest Buenas Practicas
- Rest es orientado a recursos, por tanto, poner plurales en las URI
- Entregar codigos HTTP adecuados
- No anidar mas de tres niveles de recursos
- Tener un JSON claro de maximo dos - tres niveles de anidacion
- Integrar paginacion
- Integrar Sorting
- Integrar filtros
- Documentar la API
	- Preferentemente OPEN API - Swagger
- Generar links de Navegacion
	- Preferentemente siguiendo HATEOAS
- Asegurar la API definiendo roles (seguridad)
- Exportar clientes de demostracion
	- Preferentemente usando POSTMAN
- Entregar errores definidos y verbosos
- Validacion de Campos
- Versionado de la API

## Externalizacion
La externalizacionc es un proceso en el cual se pasan las propiedades que son ajenas al codigo a archivos de texto plano que pueden ser importados hacia el codigo.

En Spring la externalizacion se hace a archivos de texto plano con terminacion .properties (app.properties, config.properties, etc).

Para acceder a ellos se utiliza SpEL y regularmente se crean Beans a partir de estas propiedades en texto plano. 

## OpenAPI - Swagger
Es un conjunto de aplicaciones que sirven para generar codigo y documentacion interactiva siguiendo el estandar de OpenAPI.

En Spring puede ser integrada para hacer ingenieria inversa, es decir, generar un documento Swagger a partir de una API ya establecida.  Para ello existe una libreria llamada springfox

## HATEOAS
Es una integracion que sirve para hacer Restful APIs navegables.

## Java Bean Validation - JSR 380
Sirve para validar los datos que son insertados por un usuario, regularmente estos validadores se mantienen en el DTO y se manejan con anotaciones.
- @Regex
- @Positive
- @Min
- @Max
- @Size
- @NotNull
- @NotBlank
- 









