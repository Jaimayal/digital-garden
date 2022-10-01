---
title: "Diseño Modular"
date: "2022-09-20 08:42"
tags: 
  - ooad
  - programming
draft: true
---
Es el nivel posterior al [Diseño en Codigo](notes/Dise%C3%B1o%20en%20Codigo.md), aparte de ser codigo bien inspirado del modelo del dominio que es altamente legible, se agrega que son modulos (o piezas) de codigo que tienen un tamaño homogeneo con alta cohesion y poco acoplamiento. 

Es decir, piezas que tienen un tamaño similar, en el cual cada una ejerce una sola y unica funcion que se acopla con muy pocas piezas porque no es un experto que tiene que realizar todo en la aplicacion.

Para hacerlo aprovecha e impulsa la abstraccion, encapsulacion, modularidad y jerarquia, busca finalmente crear modulos de alta calidad, es decir, que tengan alta [Mantenibilidad](Mantenibilidad.md)] (escalabilidad, calidad, reusabilidad, etc).

## Abuso del Patron Experto en la Informacion
Esta forma de diseño surge principalmente por un excesivo abuso del [Patron Experto en la Informacion](notes/Patron%20Experto%20en%20la%20Informacion.md), de ese modo, una clase puede llegar a tener un acoplamiento excesivo y puede crear clases muy complejas que colabora no solo con una sino con muchas tecnologias y clases a la vez.

Y no solo eso, sino que acoplas la clase que tiene la informacion con determinada tecnologia de modo que no puede utilizar piezas intercambiables (otro tipo de vista, otro tipo de persistencia, de seguridad, etc).

## Criterios
Esta disciplina del diseño recupera tres conceptos recurrentes.
- Cohesion (Maxima)
- Acoplamiento (Menor)
- Tamaño (Poco)

Una buena aplicacion de estos criterios resulta en clases altamente cohesivas y pocamente acopladas, con un bajo tamaño. Es decir, respetando al maximo el [[Principio KISS]]
## Cohesion
Es una medida que nos sirve para determinar que tantas responsabilidades tiene un modulo y que tanto se relacionan entre ellas.

- Una clase con alta cohesion tiene las responsabilidades minimas estrechamente relacionadas. Es decir, tiene un minimo numero de metodos altamente relacionados entre si.

Este elemento es fundamental, se encuentra en todos lados, las nuevas arquitecturas de microservicios por ejemplo, en el que cada uno es dedicado a cierta funcionalidad exponiendo la minima cantidad de cosas que se relacionan estrechamente entre si.

Objetivos:
- Pocas funcionalidades
- Altamente relacionadas

## Acoplamiento
Es otra medida que nos sirve para determinar la cantidad de [[notes/Relaciones entre Clases (Gestion de Dependencias)]] que tiene un modulo con otro. 

Tener un bajo acoplamiento infiere que existen la minima cantidad de dependencias o colaboracion para llevar acabo la responsabilidad que le concierne.

De este modo, permite que, si una pieza es reemplazada solo sea afectada la minima cantida de modulos porque sus dependencias son muy pocas.

### Acoplamiento Directo
Son todos aquellos dados en cualquier [[notes/Relaciones entre Clases por Colaboracion]] o [[notes/Relaciones entre Clases por Herencia]].

Es decir, para una clase A esta acoplada de una clase B si:
- La tiene como atributo
- La tiene como parametro de un metodo
- La tiene como variable local dentro de un metodo
- La devuelve de un metodo
- Es derivada de ella
- Utiliza sus metodos estaticos

### Acoplamiento Indirecto
Ocurre cuando:
1. Clase A tiene una dependencia directa con la clase B. Y ademas, esta 
2. Clase B en uno de sus metodos retorna una clase C
3. Clase A utiliza este metodo de la Clase B
4. Ahora la clase C es utilizada en la clase A de forma indirecta

```Java
class A {}

class B {}

class C {
	//...
	void someMethods();
}
```
