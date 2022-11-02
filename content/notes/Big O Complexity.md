---
title: "Big O"
date: "2022-11-02 08:30"
tags: 
  - algorithms
draft: true
---
Es un criterio que sirve para **categorizar la eficiencia de un algoritmo (en tiempo o espacio), basandose en que tan bien escala respecto a la informacion que recibe de entrada**. No se una medida exacta, es solo una forma de generalizar.

Usualmente, este criterio muesta el **peor caso (worst-case scenario)**, es decir, en el peor de los casos con que complejidad creceria un algoritmo.

Emplearla nos ayuda a tomar decisiones respecto a las estructuras de datos y algoritmos que utilizamos para escribir codigo.

## Ejemplo
El ejemplo a continuacion tiene Big O(n), es decir, crece de forma lineal respecto a la informacion que recibe

```Java
public static int sum(int[] arr) {
	int sum = 0;
	for (int i = 0; i < arr.length; i++) {
		sum += arr[i];
	}

	return sum;
}
```

El truco mas facil es identificar los loops, estos daran una nocion de el Big O de un algoritmo.

Sin embargo, para describirlo correctamente, es adecuado **ignorar las constantes**, es decir, en un algoritmo como:

```Java
public static int sum(int[] arr) {
	int sum = 0;
	
	for (int i = 0; i < arr.length; i++) {
		sum += arr[i];
	}

	for (int i = 0; i < arr.length; i++) {
		sum += arr[i];
	}

	return sum;
}
```

Por logica se tendria in Big O(2n), esto no es incorrecto pero para hablar de un algoritmo en muchas ocasiones **las constantes no tienen tanto impacto como un exponencial o un logaritmo, es por eso que estas son dejadas de lado**.