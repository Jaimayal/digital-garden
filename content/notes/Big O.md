---
title: "Big O"
date: "2022-11-02 08:30"
tags: 
  - algorithms
draft: false
---
Es un criterio que sirve para **categorizar la eficiencia de un algoritmo (en tiempo o espacio), basandose en que tan bien escala respecto a la informacion que recibe de entrada (n)**. No se una medida exacta, es solo una forma de generalizar.

No es suficiente con saber la diferencia de tiempo entre dos algoritmos dada cierta cantidad de informacion, debido a que cada algoritmo crecera de forma diferente mientras mayor sea la informacion. Por ejemplo, no es lo mismo comparar [[notes/Linear Search]] y [[notes/Binary Search]] con 100 elementos (donde el Binary Search es 15 veces mas rapido) a compararlo con 1billon de elementos (donde el Binary Search es 33 millones de veces mas rapido). Por eso se necesita comparar como incrementa el tiempo de cada uno respecto a la informacion que recibe.

Usualmente, este criterio muesta el **peor caso (worst-case scenario)**, es decir, en el peor de los casos con que complejidad creceria un algoritmo.

Emplearla nos ayuda a tomar decisiones respecto a las estructuras de datos y algoritmos que utilizamos para escribir codigo.

## Visualizacion
Para observar el comportamiento de Big O podriamos plasmar una grafica en la cual:
- El eje X el volumen de los datos con los que trabaja el algoritmo.
- El eje Y la cantidad de tiempo que toma el algoritmo.

![[files/Big_O_Visualizacion.svg]]
*En la imagen podemos observar el Big O de dos algoritmos diferentes, uno con tiempo constante y el otro con tiempo cuadrado*

Ya que el Big O representa el upper bound del trabajo de un algoritmo (es decir, el peor caso), podemos hacer la afirmacion de que el algoritmo solo puede trabajar mejor que este valor (por debajo de el), y que nunca lo sobrepasar√°.

## Valores Comunes
En Big O solo hay un conjunto de valores que utilizados por los algoritmos mas populares.

![[files/Big_O_Comunes.svg]]

- O(1). Tiempo constante  
- O(log n). TIempo logaritmico. Ejemplo [[notes/Binary Search]]
- O(sqrt(n)). Tiempo raiz cuadratico  
- O(n). Tiempo lineal  Ejemplo [[notes/Linear Search]]
- O(n log(n)). Tiempo log-lineal  . Ejemplo Quicksort
- O(n^2). Tiempo cuadratico  Ejemplo Selection Sort
- O(2^n). Tiempo exponencial  
- O(n!). Tiempo factorial

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

## Principios para Identificarlo
### Ignorar las Constantes
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

### Ignorar los Terminos Peque√Īos
En un algoritmo, los terminos peque√Īos suelen marcar una minima e infima diferencia mientras mas crezca el tama√Īo de los datos, es por ello que se recomienda ignorar todos los terminos que no tengan que ver con la entrada de datos (n)

![[files/Big_O_Irrelevante.svg]]

## Consejos para Identificarlo
- Si existe un loop o varios separados sera **n**
- Si hay loops dentro de loops (anidados) sera una elevacion de n, dos loops igual a **n^2**, tres loops igual a **n^3**
- Si dentro de cualquiera de los loops hay una division por la mitad sera **log n** o **n log n**