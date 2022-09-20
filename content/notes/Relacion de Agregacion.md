---
title: "Relacion de Agregacion"
date: "2022-09-20 12:35"
tags: 
  - 
draft: true
---
Siguiendo las caracteristicas de las [[notes/Relaciones entre Clases por Colaboracion]]. La relacion por agregacion tendria las siguientes:
### Caracteristicas
#### Temporalidad - Media
La vida de la agregacion (el todo) no tiene porque coincidir con la vida de ninguno de los agregados (Las partes). 

Un grupo de estudio no deja de ser un grupo de estudio si alguien deja de asistir.
#### Fidelidad - Baja
Los agregados pueden formar parte de distintas agregaciones simultaneamente.

Alguien puede asistir a multiples grupos de estudio en distintos horarios y no por eso dejan de existir o afecta a alguno de ellos.

#### Versatilidad - Media
Los agregados pueden ser intercambiados, sin embargo esto puede llegar a afectar a la agregacion o a otros agregados.

Alguien puede ser reemplazado por otra persona en un grupo de estudio pero podrian surgir problemas porque falta coordinacion de horarios.

**Por lo anterior, la agregacion es una composicion debil**.

### Representacion en UML y Codigo
#### UML
![RelacionComposicion.PNG](files/RelacionComposicion.PNG)

#### Codigo
El todo de alguna manera se encarga de instanciar a su parte.

```Java
class Todo {
	private Parte parte;

	public Todo() {
		this.parte = new Parte(); // El mismo todo instancia su parte con alta fidelidad, alta temporalidad y poca versatilidad.
	}
}
```