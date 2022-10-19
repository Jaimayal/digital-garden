---
title: "Docker"
date: "2022-10-08 19:03"
tags: 
  - softwaredev
  - devops
draft: false
---
Es una tecnologia que te permite crear contenedores (variacion de maquinas virtuales). Propone contenedores muy ligeros que sirven para poder guardar un conjunto de tecnologias, configuracion y todo lo que se necesario para que el funcionamiento de un Software
- Cada contenedor puede heredar de una imagen base que ya tiene instalada todas las dependencias necesarias para que los microservicios corran

Propone el concepto de Imagen de Docker que representa una descripcion para como se debe de instanciar un contenedor a partir de ella (Es como la OOP por Prototitpos).

## Comandos Utiles
- docker pull \<imagen\>
- docker images
- docker run \<containerId\>
- docker push. Subir una imagen a la nube
- docker ps. Ver las instancias de contenedores corriendo
- docket stop \<containerId\>
- docker run -it \<containerId\> /bin/bash. Te deja entrar a la linea de comandos de la maquina
- docker inspect \<containerId\>. Te permite ver informacion detallada del contenedor

Con un Dockerfile te puedes crear una imagen docker desde el ciclo de vida directo de Maven.

## Referencias
[Curso de microservicios con Java y Spring Boot](reference/@%20Curso%20de%20microservicios%20con%20Java%20y%20Spring%20Boot.md)
