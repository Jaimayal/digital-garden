---
title: "$ Patrones de Diseño"
date: "2022-10-20 08:52"
tags: 
  - pattern
  - gof
draft: true
---
Hacer YAGNI en tu vida es ansiedad, te inventas problemas, miedos y cosas que te incomodan sin que siquiera pasen. Lo mismo en el Software, no te vayas inventando problemas porque te vas a quemar.
- strategy = inyeccion de dependencias = relaciones de asociacion

- A un problema recurrente una solucion reusable cambiando los detalles minimos.

###### ¿Por qué utilizar patrones?
- Ahorra tiempo
- Reusa tecnicas ya probadas infinitamente
- Te integra a una comunidad
- Expande tu conocimiento

###### ¿Cuáles son los elementos de un patron?
- Nombre. Identificador del Patron
- Problema. Lo que resuelve.
	- Motivacion: Problema y Como resolverlo. (Cual y Como)
	- Intencion: Razon de ser y que hace el patron. (Por que y que)
	- Aplicabilidad Condiciones bajo las cuales se debe aplicar. (Cuando)
- Solucion. Como lo resuelve
- Consecuencias. Compromiso por aplicarlo

## Patron Singleton
- **Nombre**: Singleton
- **Problema**. 
	- Motivacion: Para algunas clases es importante compartir una unica instancia en el sistema. 
	- Intencion: Asegurar que una clase tenga una unica instancia y proveer un punto de acceso global a ella.
	- Aplicabilidad: Debe ser exactamente una unica instancia de la clase y debe ser accesible para todos los clientes desde un punto de acceso conocido.
	- Cuando la unica instancia deberia ser extensible para que cada cliente utilice las operaciones que le competen de una forma. Esto se hace haciendo que el Singleton sea un objeto polimorfico
### Aplicacion
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

Lo fuerte aqui esque el Singleton no necesariamente tiene que ser un objeto de una clase concreta, puede ser un objeto polimorfico que, dependiendo quien lo necesite puede realizar ciertas operaciones u otras. 

La diferencia entre hacerlo asi y no utilizar metodos estaticos puros esque potencias el encapsulamiento debido a que no todos conoceran todas las operaciones del objeto y puedes aprovechar todos los mecanismos del diseño orientado a objetos (Osea, puedes hacer OpenClosed mediante Inversion de Dependencias, Segregaciuon de Interfaces y otros mecanismos) utilizando herencia y polimorfismo.