---
title: "Legibilidad del Codigo"
date: "2022-09-26 12:05"
tags: 
  - softwaredev
  - programming
draft: true
---
Es la disciplina encargada de escribir ya no las clases ni las partes especificas, es la parte del diseño que se enfoca a las lineas especificas de cada metodo, clase, etc.

## KISS - Keep It Simple, Stupid
Lo sencillo es lo que funciona, menos es mas, sencillez, simple.
- Keep it Simple Stupid 
- Keep it Small and Simple
- Keep it Short and SImple

Por cada linea que se escribe, cien mas son leidas, por tanto, escribe codigo que tu mismo y otros puedan enteder, codigo sencillo.

Lo contrario a hacer un codigo sencillo es hacer un codigo dificil de leer lo que resulta en codigo espaguetti, con intenciones oscuras o de generalidad especulativa.

Para mantenerlo simple se pueden tomar distitnas estrategias

- Hacer abstracciones de codigo dificil de leer creandole un metodo especifico
- Utilizar buenos nombres de metodos

## Formato
Es importante tener un conjunto de reglas comunes que sirvan para tener un formato de codigo homogeneo entre todos los desarrolladores.

Regularmente se recomienda utilizar un estandar de formato de codigo popular en la comunidad del lenguaje en el que programas.

## Comentarios
No comentes codigo malo, reescribelo creando nuevas funciones, distribuyendo responsabilidades entre clases u otras formas que no requieran escribir comentarios que aclaran lo que nadie va a entender, que nadie va a entender o que esta sujeto a malinterpretaciones.

## Nombrado
Los nombres de variables, metodos, funciones, clases y de todo deben de ser homogeneos, claros, sencillos, simples y suficientemente descriptivos como para que todos puedan entender lo que se engloba dentro de ese nombre (tanto de forma directa como los efectos secundarios que tiene).

- Un nombre debe revelar su intencion
- Un buen nombre lleva tiempo
- Un nombre es dinamico, se puede cambiar y adaptar
- Utiliza las palabras clave del [[notes/Modelo del Dominio]]
- Se evitan acronimos, es decir, son legibles

## Estandares
Mantener unos estandares y una unica forma de escribir el codigo de modo que todos puedan entender el codigo de todos sin añadir complejidad extra.

Existen estandares en todos los lenguajes, en Java estan las de Oracle y las de Google, en JavaScript las de Alibaba.

## Consistencia
Manten y has todas las cosas que tienen caracteristicas similares de la misma manera. Consistencia en los espacios, en los nombres, en las convenciones.

Respeta las palabras del modelo del dominio, se consistente con como habla tu cliente!

## Alertas
Manten las alertas y advertencias activadas, el compilador es tu amigo y busca ayudarte con los problemas que podrian surgir de tu codigo.

## Codigo Muerto
Codigo que no aporta nada al sistema, que lo unico que hace es llenar lineas por llenar. Codigo que pasa a estar desactualizado debido a su nula documentacion y sostenido por comentarios que no han sido mantenidos desde hace mucho tiempo. Codigo que no aporta nada al proyecto.

En caso de que el codigo se mantenga empezara a ocurrir el sindrome de las ventanas rotas.
## YAGNI - You Aint Gonna Need It
Ocurre cuando se entregan caracteristicas innecesarias que no se requieren para el proyecto.

Es una perdida de tiempo, tiempo el cual deberia ser usado en actividades de desarrollo como las pruebas, la documentacion, la programacion de funcionalidades que SI se solicitaron.

## DRY - Dont Repeat Yourself
Evitar re-codificar, re-analizar y repetir en general las partes que ya fueron desarrolladas en distintas secciones del software.

Para evitar esto se debe incurrir en la reutilizacion de cosas que ya estan escritas y probadas. Sostenerte en algo que ya hiciste.


