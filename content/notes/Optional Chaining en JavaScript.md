---
title: "Optional Chaining en JavaScript"
date: "2022-09-28 09:48"
tags: 
  - javascript
draft: false
---
Esta caracteristica introducida en ES6 ayuda cuando tenemos que estar comprobando la existencia de propiedades dentro de objetos.

## Propiedades
Esto es muy util debido a que comunmente muchos objetos suelen venir del exterior, por tanto, hay muchas propiedades opcionales que podrian estar o no en ellos. 

En lugar de tener multiples ifs o otras estructuras de chequeo anidadas podemos utilizar la siguiente sintaxis:

```JavaScript
console.log(objeto.propiedad1?.propiedad2); // Si existe propiedad1 entonces devuelde propiedad2
```

Basicamente, el signo de interrogacion antes de pasar a la siguiente propiedad indica que, se debe comprobar que esa propiedad exista (Que no sea nullish), en caso de que exista procede a la siguiente, si no existe, devuelve undefined.

De este modo evitamos TypeErrors por acceder a propiedades de un valor undefined!

## Metodos
Esta misma sintaxis tambien sirve para llamar metodos que no estamos seguros si existen o no dentro del objeto.

```JavaScript
obj.method?.(); // Checa si method existe, si no existe, no lo ejecutes, si existe procede a ejecutarlo ().
```

## Arrays
Tambien podemos aplicarlo con cualquier elemento de un array si queremos seguir encadenando propiedades / metodos / otro array

```JavaScript
console.log(array[indice]?.[indice2]);
console.log(array[indice]?.metodo?.());
console.log(array[indice]?.propiedad);
```