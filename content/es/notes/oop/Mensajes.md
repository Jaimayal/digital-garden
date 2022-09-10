---
title: Mensajes
date: "2022-08-26 15:11"
draft: false
---
Es la base sobre la cual objetos pueden interactuar con otros utilizando sus vistas publicas, es decir, sus interfaces. En ese caso, un objeto activo (El que envia el mensaje) se comunica con un objeto pasivo (El que lo recibe).

```Java
class Pasivo {
	private int valor;

	public void imprimirValor() {
		System.out.println(valor);
	}
}

class Activo {
	public static void main(String[] args) {
		Pasivo pas = new Pasivo();
		// Mensaje desde this hasta pas
		pas.imprimirValor();
	}
}
```
___