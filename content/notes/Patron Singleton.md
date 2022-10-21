---
title: "Patron Singleton"
date: "2022-10-20 12:17"
tags: 
  - designpattern
draft: false
---
***Asegurar que una clase solo tenga una unica instancia y proveer un unico punto global de acceso a ella***

## Problema
Este patron surge de la necesidad de que una clase cuente con una unica instancia para multiples clases del sistema. Al ser aplicado de forma correcta, la clase en cuestion tendra una instancia y un punto de acceso global a ella.

## Aplicabildiad
- Debe ser exactamente una unica instancia de la clase.
- Debe ser accesible por un unico punto de entrada global.
- Debe ser utilizada por mas de una clase.
- Cuando la unica instancia deberia ser extensible para que cada cliente utilice las operaciones que le competen de una forma. Esto se hace haciendo que el Singleton sea un objeto polimorfico

## Implementacion
Una clase que cuenta con sus atributos y sus metodos. Una clase normal.

Para aplicar Singleton se necesita
1. Agregar un atributo estatico que es del a misma clase en la que se encuentra "instance"
2. Agregar un metodo estatico desde el cual se puede obtener la instancia "getInstance()"
3. Hacer a los constructores privados para que solo pueda ser instanciado dentro de la misma clase
4. Implementar el metodo getInstance() inicializando el atributo instance si es null y devolviendolo o solo devolviendolo si no es null

```Java
class Printer {
	// Implementacion de Singleton
	private static Printer instance;

	public static getInstance() {
		if (Printer.instance == null) {
			Printer.instance = new Printer();
		}
	}

	// Codigo de la clase Normal
	private String atrib1;
	private int atrib2;
	private long atrib3;
	private Object atrib4;
	// ...

	private Printer() {}

	public metodo1() {
		// ...
	}

	public metodo2() {
		// ...
	}

}
```

## Detalles 
Lo fuerte aqui esque el Singleton **no necesariamente tiene que ser un objeto de una clase concreta, puede ser un objeto polimorfico** que, dependiendo quien lo necesite puede realizar ciertas operaciones u otras. 

La diferencia entre hacerlo asi y no utilizar metodos estaticos puros esque potencias el encapsulamiento debido a que no todos conoceran todas las operaciones del objeto y puedes aprovechar todos los mecanismos del diseño orientado a objetos (Osea, puedes hacer OpenClosed mediante Inversion de Dependencias, Segregaciuon de Interfaces y otros mecanismos) utilizando herencia y polimorfismo.