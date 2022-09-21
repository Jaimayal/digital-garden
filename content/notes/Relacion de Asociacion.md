---
title: "Relacion de Asociacion"
date: "2022-09-21 12:06"
tags: 
  - 
draft: true
---
NO cuenta con ningun tipo de composicion, ni debil, ni fuerte, pero a la vez, es la primera que hace que una relacion entre un cliente (objeto activo) y un servidor (objeto pasivo) persista a traves de una temporalidad mas larga.

La colaboracion ocurre cuando una clase esta constatemente interactuando con otra para poder cumplir su servicio.

En esta relacion, los asociados no hacen mas que ofrecer los servicios, la asociacion no se encarga de administrar nada de ellos mas que usar los servicios cuando les sea necesario.

### Caracteristicas
#### Temporalidad - Media
La asociacion puede nacer solo con una de las partes y despues integrar a otro asociado o cambiarlo cuando sea necesario.

#### Fidelidad - Baja
Debido a que la asociacion no crea sus partes sino que en algun momento se le es asignada otro asociado para que ejecuten sus funciones

#### Versatilidad - Media
Es estricto respecto a con quien esta asociado en particular para realizar su funcion en un momento, respeta a quien se referia y le permite en algun punto cambiar al asociado.

### Representacion en UML y Codigo
#### UML
![RelacionAsociacion.png](files/RelacionAsociacion.png)

#### Codigo
```Java
class Asociacion {
	private Asociado asociado;

	public Asociacion() {
		this.asociado = null; // Puedo iniciar sin asociado tambien y posteriormente asociarme mediante el metodo set.
	}

	public Asociacion(Asociado asociado) {
		this.setAsociado(asociado); // Aveces naci ya asociado y se me puede cambiar despues, a veces no naci asociado, pero el metodo set siempre esta disponible.
	}

	public void setAsociado(Asociado asociado) {
		this.asociado = asociado; // Metodo set para actualizar mi asociado
	}

}
```

