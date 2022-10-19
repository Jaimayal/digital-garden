---
title: "Call Stack"
date: "2022-09-23 14:03"
tags: 
  - programming
draft: false
---
Es la forma en que un compilador trabaja con el llamado y la ejecucion de funciones. Mediante ella, **se sabe que funcion se ejecuta primero, quien esta esperando su resultado y quien sigue posteriormente**.

Cuando se llama a una funcion, lo que pasa en el Call Stack es que se crea un Stack Frame (tambien llamado Function Frame o **Execution Context en JavaScript**), el cual contiene todos los datos sobre una funcion como sus parametros, el valor de retorno, nombre, memoria entre otras cosas.

El ultimo componente del Call Stack es el Active Frame, este concepto se refiere a un Stack Frame que se encuentra en la cabeza del Stack, es decir, el que va a ser ejecutado primero o mas bien, el que se encuentra activo.

Entendiendo esto, veamos **como funciona el Call Stack**:
1. Mientras se van llamando las funciones se *pushean* los Stack Frames respectivos para cada una hacia el Call Stack.
2. Se asigna el Active Frame al Stack Frame que esta en la cabeza del Call Stack.
3. Posteriormente se ejecuta el Active Frame hasta que es *popped* (regularmente, cuando un valor final es retornado), 
4. Finalmente el Active Frame pasa a ser el siguiente Frame del Stack y el Call Stack total se va reduciendo hasta llegar a 0.

Entender esto nos sirve para entender como es que funciona la recursividad, mientras mas se van llamando las funciones (recursivamente), se va llenando el Call Stack hasta que se alcanza el Caso Base y se empiezan a retornar valores, cuyos resultados son encadenados hasta obtener el valor final el cual es el resultado de todos los retornos de las funciones recursivas.

Es una parte del [[notes/JavaScript Engine]], representado por una estructura de datos 'Stack'.
