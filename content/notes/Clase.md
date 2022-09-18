---
title: Clase
date: "2022-08-26 15:12"
tags:  
  - oop
draft: false
---
Las clases son un concepto basico de la programacion orientada a objetos. Una clase es un molde del cual podemos instanciar (crear, generar, construir, inicializar) objetos de ese tipo en particular. Este describe las operaciones y los datos que contendran los objetos que se instancien a partir de ella.

Fundamentalmente una clase se compone de dos cosas:
- Atributos. Son los datos que encapsula una clase
- Metodos. Son las acciones que puede ejecutar una clase

Adicionalmente, una clase esta compuesta por una vista publica y una vista privada. 
- La vista publica representa una interfaz con la que otros objetos pueden interactuar, es el medio por el cual existe la comunicacion en la POO.
- La vista privada representa todo lo que una clase encapsula, que es irrelevante para el mundo exterior y que se busca proteger de cambios malintencionados, suelen ser los datos (los cuales pueden ser otras clases o primitivos).

Una clase tambien esta compuesta por uno o mas constructores, que son la base para inicializar los objetos.
- Un constructor es como un metodo especial que sirve para brindar valores iniciales a una instancia en particular.

A partir de una clase pueden ser instanciados objetos, cada objeto tendra sus propios miembros privados y publicos provenientes de su clase.

```Java
class Fecha {
	// Vista privada
	private int dia;
	private int mes;
	private int anio;

	// Constructor
	public Fecha(int dia, int mes, int anio) {
		this.dia = dia;
		this.mes = mes;
		this.anio = anio;
	}

	// Vista publica
	public void imprimirFecha() {
		System.out.println(dia + "/" + mes + "/" + anio);
	}
}
```