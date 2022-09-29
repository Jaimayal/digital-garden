---
title: "Metodos y Practicas de Strings en JavaScript"
date: "2022-09-28 19:55"
tags: 
  - javascript
draft: true
---
Aunque en JavaScript los strings son primitivos estos tienen metodos debido a que aprovecha el mecanismo del boxing.

Por tanto, nuestro string primitivo es enboxeado en el objeto String.

- Acceso mediante corchetes
- length. Propiedad length
- indexOf. Obtener indice de la primer ocurrencia de un substring
- lastIndexOf. Obtener indice de la ultima ocurrencia de un substring
- slice. Extraer un substring (inicio inclusivo final exclusivo)
- toLowerCase. Convierte el string a lower case
- toUpperCase. Convierte el string a upper case
- trim. Remueve los espacios del principio y el final del string
- replace. Reemplaza la primer instancia de una expresion (string o regex) dentro del string.
- replaceAll. Reemplaza todas las instancias de una expreion dentro deun string.
- includes. Devuelve true o falsa si el string incluye el substring
- startsWith. Devuelve true o falsa si el string inicia con
- endsWith. Devuelve true o falsa si el string inicia con
- split. Dividir un string en multiples partes basado en un divisor (Lo podemos combinar con el mecanismo de [[notes/Destructuring en JavaScript]] debido a que retorna un array).
- join. Une multiples strings con el caracter especificado en el parametro de este metodo.
- padStart. Agrega el caracter dado al inicio hasta cumplir con la longitud indicada
- padEnd. Agrega el caracter dado al final hasta cumplir con la longitud indicada
- repeat. Duplica el string dentro de si mismo


```JavaScript
const price = '$333'
price = price.replace('$', 'MXN');
```
