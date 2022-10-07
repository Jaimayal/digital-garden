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

### Arquitectura Orientada a Microservicios
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
