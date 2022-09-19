---
title: "Metodo"
date: "2022-09-01 19:46"
tags: 
  - oop
draft: false
---
Define las operaciones (funciones, rutinas, operaciones) implantadas dentro de una clase que estaran disponibles para ser ejecutadas por los objetos que se generen de ella.

Los metodos conforman la interfaz publica de una clase, para esto, utilizan el modificador de vista publica (==public==). Todos los metodos declarados con este estan disponibles para que objetos de otra [Clase](es/notes/Clase.md) o de su misma, puedan comunicarse usando [Mensajes](notes/Mensajes.md)

Adicionalmente, tambien pueden servir como intermediario para otras operaciones si se especifican con el modificador de vista privada, de esta forma permite que desde un metodo publico se llamen a otros metodos privados

```Java {title="Date.java"}
class Date {
	private int day;

	// Parte de la vista privada
	private void print(Object value) {
		System.out.println(value);
	}

	// Parte de la vista publica / interfaz publica
	public void printDay() {
		// uso de un metodo privado para abstraer todavia mas
		print(this.day);
	}
}
```
