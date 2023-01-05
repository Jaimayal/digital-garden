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
Como ya sabemos, los arrays en PHP asignan keys numericas basadas en indice 0 en caso de no asignar una nosotros manualmente.

Sin embargo, PHP ofrece la facilidad de crear un array asociativo unicamente cambiando la sintaxis en como se define un poco:

```PHP
$array = [
	'key' => 'value',
	'key' => 'value',
	'key' => 'value',
]
```

### Remover
Para remover un elemento tenemos dos metodos bastante utiles array_pop y array_shift.
```PHP
$array = ['A'. 'B', 'C', 'D'];
echo array_shift($array); // A
echo array_pop($array); // D
```

La diferencia esque array_shift tiene que re-indexar todos los indices del array, por tanto, si se tienen numeros arbitrarios a la secuencia original estos seran reasignados y seguiran la secuencia original iniciando en cero.

Como extra, tenemos una funcion que sirve para liberar memoria llamada unset() a esta funcion podemos mandarle un array con una llave y removera dicho valor del array al liberar su memoria
```PHP
unset($array[1]) // B
```

Utilizando esta funcion el array no es reindexado, con lo que las llaves se preservan y la secuencia tambien.

## Operadores
### Aritmetica
PHP cuenta con multiples operadores aritmeticos, los principales:
- +. Suma
- -. Resta
- \*. Multiplicacion
- /. Division
- \*\*. Potencia

Un detalle importante a tener en cuenta esque el operador modulo (%) castea todo a integers, por tanto, si se trata de buscar el modulo de dos numeros flotantes se debe utilizar la funcion fmod(a, b)
```PHP
echo fmod(10.5, 2.5) // 1.80003
```

### Strings
Los Strings tienen un unico operador que sirve para concatenar, tambien lo tienen en forma de apender al final de string:
```PHP
$h = 'Hello'
$h = $h . ' World'; // Hello World
$h .= '!'; // Hello World!
```

### Comparacion
Al igual que en JavaScript existen dos operadores para hacer comparacion directa:
- ==
- ===
El primero hace conversion de tipos y tiene comportamiento no deseado, usualmente, se recomienda utilizar el tercero.
```PHP
var_dump(3 === '3') // false
var_dump(3 == '3') // true
```

Existe un operador bastante extraño llamado spaceship operator que retorna un valor -1, 0 o 1 en dependiendo de si un valor es mayor, menor o igual que otro
```PHP
var_dump(3 <=> 5); // -1
var_dump(3 <=> 3); // 0
var_dump(3 <=> 1); // 1
```

Null Coalescing
Es otro operador que nos sirve para dar un valor por defecto en caso de encontrarnos con un null.
```PHP
$x = null;
$y = $x ?? 'El valor era null';
echo $y; // El valor era null
```

## Operadores Bitwise
Son operadores que sirven para realizar operaciones a nivel de bit, binarios. Sirven para hacer aritmetica con numeros a nivel de los bits.

## Operadores Array
Existen operadores que sirven para manipular arrays.
- +. Union. Apende los elementos del segundo array a los del primero en caso de que sus keys no se encuentren existentes en el
- \=\=. Compara valores y llaves entre dos arrays, unicamente retornara true si todos los valores coinciden
- \=\=\=. Compara los valores y llaves entre dos arrays pero sin realizar conversion de tipos, es decir, es mas estricto

