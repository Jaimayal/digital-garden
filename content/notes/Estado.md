---
title: Estado
date: "2022-08-26 15:11"
tags: 
  - oop
draft: false
---
Se refiere a los valores que tiene el conjunto de datos que encontramos en un objeto en determinado momento. 

Regularmente el estado lo podemos comprobar mediante la interfaz publica especificada en la clase del objeto al que queremos consultar, imaginando que en algun lugar existe la clase fecha podriamos hacer:

```Java
class Main {
	public static void main(String[] args) {
		Fecha fecha = new Fecha(1, 1, 2002);
		// Consulta de Estado
		fecha.imprimirFecha();
	}
}
```