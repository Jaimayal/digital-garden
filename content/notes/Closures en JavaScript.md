---
title: "Closures en JavaScript"
date: "2022-09-30 10:20"
tags: 
  - javascript
draft: true
---
Es una caracteristica especial de las [[notes/Funciones en JavaScript]] que combina los [[notes/JavaScript Execution Context]], el [[notes/Call Stack]]y los [[notes/Scope]] .

Es un fenomeno que ocurre gracias a las [[notes/Funciones de Primera Clase]]. 

**Basicamente un closure es la conexion que existe entre una funcion y el variable environment que existia cuando fue asignada**. Este **tiene prioridad sobre cualquier otro [[notes/Scope]]**.

![[files/Closure.png]]

```JavaScript
const secureBooking = function() {
	let passengerCount = 0;

	return function() {
		passengerCount++;
		console.log(`${passengerCount}`);
	}

	const booker = secureBooking();
	booker();
}
```

Aun si donde fue creada ya no existe, sigue manteniendo las referencias y valores que le fueron asignados (o heredados) como propios.