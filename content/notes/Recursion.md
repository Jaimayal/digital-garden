---
title: "Recursion"
date: "2022-11-04 10:57"
tags: 
  - programming
draft: true
---
Se trata de una tecnica de programacion en la cual una funcion, metodo o subrutina (dependiendo del paradigma que estemos llevando a cabo), que, para llevar acabo sus funciones, se llama a si misma.

Esta tecnica ocupa mas memoria que utilizar un loop, usualmente todo lo que puede ser realizado Recursivamente tiene al menos otra solucion un poco mas eficiente (con loop)

En caso de querer utilizar esta tecnica, lo que debemos hacer es contar con dos situaciones:

1.  Base Case. En esta parte del algoritmo se determina el caso base, es la forma en que podemos prevenir entrar a un loop infinito, se define el elemento al cual todos los casos recursivos van a llegar.
2.  Recursive Case. En caso de no cumplir el caso base entonces se entrara al caso recursivo, en este caso lo que se realiza es un llamado a la misma funcion que esta ejecutando la rutina, entrando dentro de si misma una y otra vez hasta que cada llamado a la funcion llegue al caso base, una vez ahi, se empezaran a retornar los valores hasta obtener un resultado.

Veamos un ejemplo matematico con el clasico factorial (n!) en C.

```c
int factorial(int n)
{
	if (n == 1) // Caso base
	{
		return 1;
	}

	return n * factorial(n - 1); // Caso recursivo
}
```
