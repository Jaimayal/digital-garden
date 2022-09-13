---
title: Atributos
date: "2022-08-26 15:11"
draft: false
---
Constituyen los datos particulares de una clase, pueden estar soportados por tipos primitivos (int, char, boolean, float, double, etc) o pueden estar soportados por otras clases.

Estos suelen estar ocultos mediante el uso de la vista privada para evitar errores, mejorar seguridad, hacer efectivo el encapsulamiento y abstraer para reducir la complejidad de una clase.

```Java
class Fecha {
	// Lista de atributos
	private int dia;
	private int mes;
	private int anio;
}
```