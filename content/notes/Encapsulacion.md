---
title: "Encapsulacion"
date: "2022-10-22 10:37"
tags: 
  - softwaredev
  - oop
draft: true
---
La encapsulacion es un proceso en el cual se aprovechan los resultados de la abstraccion. Lo que se hace esque:
1. Se crea una capsula (usualmente, una clase) que guarde los datos y operaciones que hace un objeto.
2. Se expone una interfaz publica de operaciones disponibles para que otros interactuen con el objeto
3. Se ocultan los detalles de los procesos internos y los datos dentro de la capsula
## Objetivo
Crear un efecto de caja negra, en el cual nosotros solo damos entradas y esperamos una salida, sin saber el proceso que ocurre en medio.

## Ejemplo
Al solicitarle las califaciones a un Estudiante no sabemos si va a colaborar con otros (Administracion, ventanilla virtual, pagina de su universidad) o lo va a hacer el mismo (Quiza porque hizo un papel de toda su trayectoria escolar), todo lo que sabemos esque de alguna forma se nos proporcionara las califaciones del estudiante sin saber como lo hizo.

## Resultado
Al aplicarla se forma un objeto que encapsula datos y operaciones. A la vez, este mismo expone una interfaz y oculta implementaciones y datos.

Esto hace que:
- Se **incremente la flexibilidad** debido a que, mientras se cumplan las operaciones de la interfaz, no importa como esta implementado de fondo
- Se **incrementa la seguridad** porque la misma clase tiene control de quien accede a sus elementos
- Se **conserva la integridad de los datos** debido a que la misma clase controla las operaciones que pasan con los datos que guarda.