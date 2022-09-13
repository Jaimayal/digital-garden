---
title: "Constructores"
date: "2022-09-05 14:57"
tags:
  - programming
  - oop
draft: true
---
Popularmente llamados "constructores" son metodos especiales en el codigo que sirven como **inicializadores de objetos**. Buscan crear instancias especificas de una clase, una instancia en particular tambien es llamada [Objeto](es/notes/oop/Objeto.md). Los constructores ademas son encargados de que todas las instancias sean **estables** inicializando todos los atributos de su clase a un valor especifico.

```Java
class SomeClass {
	private int value

	// Constructor
	public SomeClass() {
		this.value = 1;
	}
}
```

Es buena practica inicializar todos los atributos y no depender de funciones del compilador. 

Tambien es considerada buena practica integrar al menos un constructor y no recaer en el default constructor dado por el compilador en caso de que no tengamos ninguno en nuestra clase.