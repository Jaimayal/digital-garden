---
title: "Inversion de Control"
date: "2022-10-28 17:37"
tags: 
  - oop
draft: false
---
Cuando escribimos codigo normalmente nosotros hacemos llamada a las distintas librerias y partes que nosotros queremos a lo largo de nuestro programa, en otras palabras "Nosotros tenemos el control sobre lo que utilizamos y lo que no".

**No nos llames, nosotros te llamamos.**

La Inversion de Control propone lo que su nombre menciona, es decir, el codigo que nosotros escribamos sera llamado por el framework, sera orquestado junto con otras librerias y aplicara la configuracion para tener una aplicacion completa y lista para ser utilizada.

Para alcanzar el IoC tenemos distintos mecanismos como "Strategy", "Service Locator", "Factory" o "[[Dependency Injection]]", en concreto este ultimo es una parte muy importante de Spring.

Otro ejemplo de IoC es el [[notes/Template Method (Metodo Plantilla)]], este consigue la Inversion de Control debido a que el control se encuentra en la clase abstracta que cuenta con los metodos definidos en las clases concretas. Las clases concretas desconocen cuando su codigo sera llamado.

## Ventajas
- Separa la ejecucion de la implementacion de una tarea.
- Permitir un facil Mockeo de nuestros objetos para que sean mas facilmente probados.
- Mejora la modularidad (Hace piezas pocamente acopladas, altamente cohesivas).
- Permite reemplazar la misma pieza de codigo con distintas implementaciones