---
title: "Acoplamiento"
date: "2022-10-22 14:55"
tags: 
  - softwaredev
draft: true
---
Es una medidaque nos sirve para determinar la cantidad de [[notes/Relaciones entre Clases (Gestion de Dependencias)]] que tiene un modulo con otro. 

Existe una estrecha relacion con la [[notes/Cohesion]]. Regularmente, una clase altamente cohesiva tendra un menor numero de clases acopladas. 

Aplicarlo correctamente permite el reemplazo de piezas en cualquier parte del software, debido a que solo se afectarian una minima cantidad de modulos.

Tener un bajo acoplamiento infiere que existen la minima cantidad de dependencias o colaboracion para llevar acabo la responsabilidad que le concierne. Especialmente se busca un bajo acoplamiento de clases que son inestables y que pueden tender a ser cambiadas a futuro (de interfaz o de implementacion).

Existen distintos tipos de acoplamiento. Los tipos son:
## Por su Visibilidad
- [[notes/Acoplamiento Directo]]
- [[notes/Acoplamiento Indirecto]]

## Por su Direccion
- [[notes/Acoplamiento Aferente]]
- [[notes/Acoplamiento Eferente]]

## Excepciones
Se puede permitir el acoplamiento alto si:
- Las clases a las que estoy acoplado son muy estables y generalizadas (como libreria de Java)
- Las clases a las que estoy acoplado no van a cambiar en los requisitos

Normalmente habra un grado medio de acoplamiento si estoy trabajando para realizar mis funciones

___
Complejidad entre un modulo y otros modulos

Cantidad de modulos (se busc abaja)
Obviedad de las conexiones (se busca alta)
Flexibilidad que tan facil es intercambiar otros modulos (se busca alta)