---
title: "Microservicios"
date: "2022-10-08 19:01"
tags: 
  - softwaredev
draft: true
---
Es un tipo de arquitectura de Software, algunas de sus caracteristicas principales son:
- Dividir toda la solucion en multiples modulos llamados microservicios en el que cada uno resuelve una funcionalidad.
- Los microservicios se comunican regularmente mediante REST o sistemas de mensajeria como RabbitMQ.
- Se logra muy bajo acoplamiento afernte y eferente.
- Aumenta la complejidad de despliegue{
- Desarrollo puede ser agnostico al lenguaje
- Permite reutilizarse en distintas soluciones para problemas.

Anatomia tipica de un Microservicio
![[files/ComponentesMicroservicio.png]]

La capa Controller solo debe encargarse de enviar los datos que recibe del mundo exterior a la capa Service.

La capa Service debe contener toda la logica de negocio.

La capa DAO unicamente debe encargarse de comunicarse con la persistencia de la aplicacion

___

## Referencias
[Curso de microservicios con Java y Spring Boot](reference/@%20Curso%20de%20microservicios%20con%20Java%20y%20Spring%20Boot.md)