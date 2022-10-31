---
title: "The Complete JavaScript Course 2022: From Zero to Expert!"
date: "2022-10-31 09:20"
tags: 
  - 
draft: true
---
## Converting and Checking Numbers
Los numeros decimales en JavaScript van muy bugeados, no sirve para hacer calculos exactos con fracciones en el sistema decimal de 10s

Otra practica "sucia" en JavaScript es reemplazar la conversion explicita (Utilizando Number()) por una conversion del lenguaje utilizando el simbolo + antes de un String como:

```JavaScript
const number = +'23';
console.log(typeof number); // number
```

Pero eso no es todo, ademas existe una forma de castear pero removiendo letras que esten dentro de un String

```JavaScript
const numberParsed = Number.parseInt('30px'); // 30
const numberRadixBinary = Number.parseInt('30', 4); // Binario

const decimalParsed = Number.parseFloat('2.5rem'); // 2.6
```

Ademas podemos checar si un numero es NaN (Unvalor falsy)

```JavaScript
const isNan = Number.isNaN(20); // false
const isNan2 = Number.isNaN('20'); // false
const isNan3 = Number.isNaN(+'hola'); // true
const isNan4 = Number.isNaN(23 / 0); // false
```

Sin embargo, la mejor forma de saber si un valor es un numero es utilizando isFinite, este retorna false para NaN e Infinite.

```JavaScript
const isFinite = Number.isFinite(20); // true
const isFinite2 = Number.isFinite(23 / 0); // false
const isFinite3 = Number.isFinite(+'hola'); // false
```

## Math and Rounding
Math.max
Math.min
Math.sqrt

Math.random

Constants 
Math.PI

Existe un metodo que arregla el numero de decimales que debe tener un numero
```JavaScript
const round = +(2.3).toFixed(3); // 2.300
```

Adicionalmente, existe un separador numerico especial que sirve para diferenciar los numeros unos de otros. El separador es el simbolo '\_';

```JavaScript
console.log(200_000); // 200,000
```

BigInt agrega las capacidades de trabajar con numeros extremadamente grandes. Para utilizarlo se puede utilizar el casteo con la funcion BigInt() o agregando una 'n' al final de un numero

```JavaScript
const hugeNumber = 12893712983712893172489326757834n;
```

Trabajar con fechas tambien es bastante simple. Existe el objeto Date con multiples constructores, puede convertirlo desde un Timestamp, desde un String o desde un nuermo de anios, meses, dias, etc.

Adicionalmente, podemos hacer calculaciones sobre ellas gracias a las timestamps!