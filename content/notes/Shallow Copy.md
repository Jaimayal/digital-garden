---
title: "Shallow Copy"
date: "2022-09-25 11:03"
tags: 
  - programming
draft: false
---
Tipo de clonado de un objeto que ocurre cuando solo se logra clonar los atributos superficiales, las referencias internas que componen al objeto no cambiaran, solo lo superficial.

### JavaScript
La forma de hacer shallow copy en JavaScript es utilizando el metodo Object.assign.

```JavaScript
const original = {
	firstName: 'Jaime',
	lastName: 'Ayala',
	family: ['Pepe', 'Mari']
};

const clone = Object.assign({}, original);
clone.lastName = 'Perez'; // Solo cambia clone
clone.family.push('Luz'); // Cambia clone y original

console.log(original);// Jaime Ayala ['Pepe', 'Mari', 'Luz']
console.log(clone); // Jaime Perez ['Pepe', 'Mari', 'Luz']
```