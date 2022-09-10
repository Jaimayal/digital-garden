---
title: Metodos
date: "2022-08-26 15:11"
draft: false
---
Se refiere a las operaciones que constituyen una [[Clase]] en particular. Regularmente encontramos metodos publicos que representan la interfaz que sirve para enviar [[Mensajes]] entre objetos y una vista privada que sirve para realizar abstracciones de operaciones dentro de una misma clase.

Veamos dos metodos, uno publico y uno privado.
```Java
class Main {
	// Vista Publica
	public void imprimirNumero(int numero) {
		System.out.println(numero);
		imprimirFinalizado();
	}

	// Vista Privada
	private void imprimirFinalizado() {
		System.out.println("Finalizado :)");
	}
}
```

___