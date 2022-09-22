---
title: "Relacion de Uso (Dependencia)"
date: "2022-09-21 12:37"
tags: 
  - 
draft: true
---
Este tipo de relacion ocurre cuando una clase A utiliza los servicios de una clase B en algun punto especifico sin mayor dependencia a futuro.

## Caracteristicas
### Temporalidad - Baja
Es momentanea, solo por un ratito y no dura casi nada mas que para satisfacer una necesidad especifica en un momento especifico.

### Fidelidad - Variante
Se puede utilizar algo tanto publico como privado, pero como la relacion es tan corta no resulta tan relevante.

### Versatilidad - Alta
El usador puede utilizar a cualquiera que ofrezca los mismos servicios que el usado, sin importar quien sea.

## Representaicon en UML y Codigo
### UML
![RelacionUso.png](files/RelacionUso.png)

### Codigo
```Java
class Usador {
	// Puede haber un usado por parametro
	public Usador(Usado usado) { 
		Usado local = new Usado(); // O un usado local que me sirve para inicializar otras cosas
		//...
	}
}
```