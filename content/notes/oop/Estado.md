---
title: "Estado"
date: "2022-09-01 19:46"
tags: 
draft: true
---
# Estado
Se refiere al conjunto de datos (formalmente llamados [[Atributos]]) que conforman un ==objeto== y que tienen valores en un determinado momento.

Regularmente un objeto le pregunta a otro su estado mediante un [[Mensaje]] (una llamada a los metodos de su clase).

Suponiendo que existe la clase "Date" en algun lado, veamos como se le consulta su estado

```Java {title="Main.java"}
class Main {
	public static void main(String[] args) {
		Date date = new Date(30, 9, 2000);
		date.printFullDate(); // 30-09-2000
	}
}
```
___
