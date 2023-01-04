---
title: "PHP"
date: "2023-01-04 11:30"
tags: 
  - php
draft: false
---
## Sintaxis Basica
Para reconocer bloques de codigo PHP utiliza la sintaxis \<?php  // codigo ?>

## Imprimir a pantalla
Existen dos funciones que sirven para imprimir por pantalla:
```PHP
echo();
print();
```

La diferencia entre estas es que print nos permite imprimir texto unicamente y print nos permite imprimir valores de las variables

Ademas print retorna un valor 1 o "True"

echo puede ser utilizadas sin parentesis, esto permite concatenar multiples valores utilizando una coma
```PHP
echo 'hola', ' ', 'mundo';
```

Y variables utilizando un punto
```PHP
echo 'hola ' . $name;
```

### Imprimir Variables
Para imprimir variables debemos utilizar un string de texto entre comillas dobles, debido a que estas nos permiten imprimir por pantalla el valor de la variable
```PHP
echo "Hola me llamo {$name}"; // Funciona
echo 'Hola me llamo {$name}'; // No funciona
```

## Variables
Las variables inician con simbolos $, estas deben iniciar con letras, o guion bajo y no puede contener caracteres especiales. 

### Por valor
Ademas, las variables son asignadas por valor, con lo que si hacemos esto:
```PHP
$x = 1;
$y = $x;

$x = 3;
echo $y; // 1
```

Al final obtendremos 1 como respuesta.
### Por referencia
Por otro lado, si lo que queremos realmente es la referencia que tiene la variable podemos utilizar el operador &
```PHP
$x = 1;
$y = &$y;

$x = 3;
echo $y; // 3
```

## Constantes
Existen dos formas principales de definir constantes
- utilizando la keyword const
- utilizando la funcion define()

Estas siguen las mismas reglas de las variables y deben encontrarse escritas en mayusculas. Para referirse a ellas dentro de funciones o bloques de codigo no es necesario utilizar ningun simbolo, estas son escritas como texto plano
```PHP
define('STATUS_CODE', '200');

echo STATUS_CODE; // 200
```

### const
Este tipo de constantes se definen en tiempo de compilacion y por tanto solo pueden ser definadas al inicio del bloque de codigo de PHP. 
```

```

### define()
Este tipo de constantes pueden ser definidas en cualquier punto del codigo de PHP debido a que son definidas en tiempo de ejecucion.

## Variable de Variable
Es un tipo de variable que adquiere el nombre de forma dinamica proveniente del valor de otra variable. Se define utilizando doble simbolo de \$\$.
```PHP
$foo = 'bar';
$$foo = 'zas'; // $$foo == $bar

echo $$foo; // zas
echo $bar // zas
```

## Tipos de Datos
Hay diez tipos de datos basicos en PHP:
- bool
- int
- float
- string
- array
- object
- callable
- iterable
- resource
- null

### var_dump()
Es una funcion muy util que sirve para ver el tipo de dato y el valor que tiene una variable en tiempo de ejecucion
```PHP
$x = 2.34;
var_dump($x);
```

### type juggling / type coercion
Es un mecanismo introducido en PHP para que las funciones ejecuten una conversion al inicio del llamado, y levanten un error en caso de que se les envie un tipo de dato que no tiene casting al tipo de dato indicado.
```PHP
function sum(int $x, int $y) {
	return $x + $y;
}

echo sum(2, 3) // 5
echo sum(2.7, 3) // 5
echo sum(2, '3') // 5
```

En caso de querer que no se acepte ningun valor que no sea int (Es decir, que no se le realice ningun tipo de casting) se debe activar el **modo estricto**

### Strict mode / Strict types
Para activar el modo estricto se debe declarar la siguiente configuracion al inicio del script:
```PHP
declare(strict_types=1);
```

Con esta linea de codigo se activara el modo estricto y se hara que se respete el type juggling sin hacer ningun tipo de casting


### Casting
El casting es bastante similar a Java utilizando la sintaxis de los parentesis
```PHP
$x = (int) '5'; 
var_dump($x); // int(5)
```

### Falsy Values
En PHP tambien se cuenta con una serie de Falsy values que sirven para hacer las condicionales un poco mas faciles de aplicar si los entiendes correctamente
```PHP
// Falsy values
// 0 -0
// 0.0 -0.0
// ''
// '0'
// []
// null
```

## Array
Es una estructura de datos basica, en PHP, parece estar soportada por una lista / mapa.

```PHP
$array = ['Uno', 'Dos', 'Tres'];
```

Como todos los lenguajes de programacion, los arrays tienen un indice iniciando por cero. Si accedes a un elemento que no existe tendras el error undefined y obtendras null como resultado.

### Insertar
Para insertar un nuevo valor basta con colocar la sintaxis de los squarebrackets sin un key, esto es debido a que, si no se especifica un key asociativo, el array le dara el siguiente que se tiene disponible en la secuencia numerica.
```PHP
$array[] = 'Cuatro';
```

Otra forma es utilizando la funcion array_push()
```PHP
array_push($array, 'Cinco', 'Seis', 'Siete');
```

### Keys personalizadas
Como ya sabemos, los arrays en PHP asignan keys de forma automatica en caso de 