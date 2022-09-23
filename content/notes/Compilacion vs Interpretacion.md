---
title: "Compilacion vs Interpretacion"
date: "2022-09-23 12:51"
tags: 
  - programming
draft: true
---
Como se sabe, las computadoras solamente entienden codigo maquina (Binario, regularmente). En la [[notes/Programacion]] existen dos tipos de lenguajes que llegan a este fin de maneras diferentes, los lenguajes Compilados y los Interpretados.

## Compilacion
Para ejecutar un programa desde un codigo escrito en un lenguaje compilado tenemos que hacer dos pasos.
1. Traducir todo el codigo de una sola pasada a codigo maquina que es facilmente ejecutable
2. Ejecutar el codigo mediante el archivo resultante en cualquier momento.

![[files/Compilacion.png]]
## Interpretacion
Cada vez que el codigo es ejecutado este tiene que ser traducido linea por linea a codigo maquina y despues ser ejecutada una tras otra, es por eso que se dice que los lenguajes interpretados son tan lentos.

![[files/Interpretacion.png]]

## Just-in-Time Compiled
Es una variacion y combin acion entre la Compilacion y la Interpretacion.

En este caso, cuando se busca ejecutar codigo, primero es completamente pasado a codigo maquina y despues es ejecutado, con la caracteristica de que esta vez no obtenemos archivos intermedios portables

![[files/Just-In-Time-Compiled.png]]