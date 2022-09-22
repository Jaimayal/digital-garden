---
title: "Relacion de Agregacion"
date: "2022-09-20 12:35"
tags: 
  - ooad
draft: true
---
Siguiendo las caracteristicas de las [Relaciones entre Clases por Colaboracion](notes/Relaciones%20entre%20Clases%20por%20Colaboracion.md). La relacion por agregacion tendria las siguientes:

En esta relacion la agregacion se encarga de gestionar todo lo relacionado con los agregados una vez forman parte de ella.
## Caracteristicas
### Temporalidad - Media
La vida de la agregacion (el todo) no tiene porque coincidir con la vida de ninguno de los agregados (Las partes). 

Un grupo de estudio no deja de ser un grupo de estudio si alguien deja de asistir.
### Fidelidad - Media
Los agregados pueden formar parte de distintas agregaciones simultaneamente.

Alguien puede asistir a multiples grupos de estudio en distintos horarios y no por eso dejan de existir o afecta a alguno de ellos. Sin embargo, cada una de las agregaciones lleva su gestion de forma privada

### Versatilidad - Media
Los agregados pueden ser intercambiados, sin embargo esto puede llegar a afectar a la agregacion o a otros agregados.

Alguien puede ser reemplazado por otra persona en un grupo de estudio pero podrian surgir problemas porque falta coordinacion de horarios.

**Por lo anterior, la agregacion es una composicion debil, un agregado puede existir sin la necesidad de que exista una agregacion.**.

## Representacion en UML y Codigo
### UML
![RelacionAgregacion.PNG](files/RelacionAgregacion.PNG)

### Codigo
La agregacion es una coleccion de agregados en el que todos pueden entrar yt salir.

```Java
class Agregacion {
	private List<Agregado> agregados;

	public Todo() {
		this.agregados = new ArrayList<Agregado>(); // No se crea ningun agregado, solo la estructura para almacenarlos
	}

	public void add(Agregado agregado) {
		this.agregados.add(agregado);
	}

	public void remove(Agregado agregado) {
		this.agregados.remove(agregado);	
	}
}
```