---
title: "Relacion de Composicion"
date: "2022-09-20 12:35"
tags: 
  - 
draft: true
---
Siguiendo las caracteristicas de las [[notes/Relaciones entre Clases por Colaboracion]]. La relacion por composicion tendria las siguientes:

### Temporalidad - Alta
Regularmente, este tipo de relaciones vinculan **toda la longevidad del todo con la longevidad de la parte**. Es decir, el todo no es el todo sin sus partes.

Un ejemplo podria ser "el humano promedio tiene un sistema circulatorio, nervioso, digestivo y si le quitas uno, deja de ser un humano promedio":

### Fidelidad - Alta
Los sistemas de un humano promedio no pueden ser compartidos de forma concurrente por otro humano,

### Versatilidad - Baja
Los sistemas del humano promedio son diseñados para si mismo y no pueden ser intercambiados por maquinas u otros porque dejaria de ser un humano promedio.

**Por lo anterior, la composicion es una composicion fuerte**.

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