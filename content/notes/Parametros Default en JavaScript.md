---
title: "Parametros Default en JavaScript"
date: "2022-09-29 10:58"
tags: 
  - javascript
draft: true
---
Es una caracteristica agregada a las funciones en ES6 que permite asignar valores por defecto a los parametros en caso de que no sean brindados por el usuario.

Su sintaxis es muy intuitiva puesto que desde la funcion directamente podemos declararlos.

```JavaScript
function funcion(parametro1 = 'valorPorDefectoSiNoEsEspecificado') {
	console.log(parametro1); // parametro o valorpordefecto
}
```

