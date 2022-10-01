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

Una buena aplicacion de estos criterios resulta en clases altamente cohesivas y pocamente acopladas (acoplamiento eferente a clases inestables), con un bajo tamaño. Es decir, respetando al maximo el [[Principio KISS]]
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

### Visibilidad
#### Acoplamiento Directo
Son todos aquellos dados en cualquier [[notes/Relaciones entre Clases por Colaboracion]] o [[notes/Relaciones entre Clases por Herencia]].

Es decir, para una clase A esta acoplada de una clase B si:
- La tiene como atributo
- La tiene como parametro de un metodo
- La tiene como variable local dentro de un metodo
- La devuelve de un metodo
- Es derivada de ella
- Utiliza sus metodos estaticos

#### Acoplamiento Indirecto
Ocurre cuando:
1. Clase A tiene una dependencia directa con la clase B. Y ademas, esta 
2. Clase B en uno de sus metodos retorna una clase C
3. Clase A utiliza este metodo de la Clase B
4. Ahora la clase C es utilizada en la clase A de forma indirecta

```Java
class A {
	void main() {
		new B().getClassPerformer().someMethod(); // Acoplamiento indirecto
	}
}

class B {
	classC getClassPerformer();
}

class C {
	//...
	void someMethod();
}
```

### Direccion
#### Acoplamiento Aferente - Reusabilidad
Quienes dependen de mi para realizar sus funciones, ya sea por colaboracion, por herencia o por acoplamiento indirecto.
- Cuando esta clase es la usada en una relacion de uso
- Cuando esta clase es una parte de una relacion de composicion
- Cuando esta clase es el asociado en una relacion de asociacion
- Cuando esta clase es padre de otras clases.

#### Acoplamiento Eferente - Dependencias  
De quien dependeno para reaizar mi funcion, se identifica mediante relaciones de colaboracion, herencia o por acoplamiento indirecto.
- Cuando esta clase es la que usa a otras en una relacion de uso
- Cuando esta clase es el todo en una relacion de composicion
- Cuando esta clase es la que requiere de un asociado en una relacion de asociacion
- Cuando esta clase es hija de una superclase.

Se puede permitir el acoplamiento alto si:
- Las clases a las que estoy acoplado son muy estables y generalizadas (como libreria de Java)

Normalmente habra un grado medio de acoplamiento si estoy trabajando para realizar mis funciones

Se busca un bajo acoplamiento de clases que son inestables y que pueden tender a ser cambiadas a futuro (de interfaz o de implementacion).

Estas propiedades estan fuertemente relacionadas, si se impulsa para bien una de ellas de forma inferente se impulsara la otra.

## Tamaño
Sirven como una referencia a tener en cuenta para escribir codigo de calidad, no se deben seguir a rajatabla sin embargo establecen un punto de partida para permitir identificar codigo de calidad.

- Paquete - 12 a 20 clases
- Clase - 3 a 5 atributos
- Clase - 15 a 25 metodos
- Clase - 200 a 500 lineas
- Metodo - 1 a 3 parametros
- Metodo - 10 a 25 lineas
- Metodo - 2 a 3 sentencias anidadas
- Linea - 80 a 120 caracteres

**Son solo valores orientativos**.
