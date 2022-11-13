---
title: "Diseño por Contrato"
date: "2022-10-28 16:51"
tags: 
  - oop
draft: false
---
El diseño por contrato establece un contrato entre dos partes, el cliente y el servidor. Regularmente, es utilizada al desarrollar la implementacion de una clase. En este caso, el cliente de un metodo es quien le esta llamando, el servidor es el que procesa la entrada y del que se espera obtener un resultado.

## Diferenciaciones
Tres terminologias
- Error. Cometido por un Humano
- Defecto. Encontrado en un Software
- Fallo. Producido por un Defecto en el software

Dos tipos de errores
- Errores Excepcionales. Que ocurren debido a fallas externas al Software
- Errores logicos. Que ocurren debido a la logica interna del programa

Dos mecanismos para lidiar con fallos
- Programacion Defensiva
- Aserciones

La programacion defensiva es poco apropiada, pero de ser implementada, puede servir finalmente como una red de aserciones.

## Buenas Practicas
El diseño por contrato concibe que estas dos partes tengan un contrato formal en el que se establecen:
1. Las precondiciones que debe de cumplir un cliente para llamar una funcion
2. Las postcondiciones que debe de cumplir el servidor y retornarle al cliente

De esta forma, las dos partes del contrato pueden estar seguras que ambas cumpliran con su parte y pueden avanzar de forma segura.

Para implementarlo se suele utilizar los assert.
