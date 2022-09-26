---
title: "Metodos de Objetos en JavaScript"
date: "2022-09-19 08:38"
tags: 
  - javascript
draft: false
---
Para crear metodos (funciones, rutinas, etc) dentro de un objeto primero debemos entender que estos no son mas que **propiedades de un objeto ya existente**. Sin embargo, recordemos que existen dos formas de declarar [Funciones en JavaScript](notes/Funciones%20en%20JavaScript.md). 

En este caso, lo que necesitamos es utilizar una Expresion Funcional (Forma normal o en flecha).

```JavaScript
const object = {
	name: 'Jaime',
	lastName: 'Ayala',

	calcAge: birthYear => 2022 - birthYear,
	calcAge2: function (birthYear) {
		return 2022 - birthYear;
	}
}
```

Ahora para llamarla podemos utilizar cualquiera de las dos formas de acceder a las [Propiedades de Objetos en JavaScript](notes/Propiedades%20de%20Objetos%20en%20JavaScript.md).

```JavaScript
console.log(object.calcAge(2002)); // 20
console.log(object['calcAge'](2002)); // 20
```

```JavaScript
const object = {
	//...
	summary: () => {
		const age = this.age ? this.age : this.calcAge();
		
		console.log(`${this.firstName} is a ${age}-year old ${this.job}, and he has ${this.hasDriversLicence ? 'a' : 'no'} driver's licence`);
	}
}
```

