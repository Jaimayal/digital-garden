---
title: "Ley de Demeter"
date: "2022-10-28 17:53"
tags: 
  - oop
draft: true
---
Son un conjunto de leyes obtenidas desde un proyecto. En el cual se dictamenta que UNICAMENTE SE PUEDE COLABORAR CON:
- this
- Parametros
- Atributos
- Objetos Locales

Por tanto, nunca se debe interactuar con un encadenamiento de mensajes obtenidas de enviar un mensaje a otro objeto. Es decir EVITAR EL ACOPLAMIENTO INDIRECTO A TODA COSTA.

## Ley Estricta de Demeter
- Ni se te ocurra hablar con los atributos de la clase base, esto para evitar acoplamiento a la clase base.
- Si es la parte critica de la aplicacion, la que mas tiende a los cambios, esta es la indicada
## Ley flexible de Demeter
- Si se te permite hablar con los atributos de la clase base. Si es una herencia pequeña esta es la indicada
